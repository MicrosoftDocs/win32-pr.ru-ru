---
description: Указывает хранилище сертификатов, используемое для подписания документа.
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: Структура SIGNER_CERT_STORE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682892"
---
# <a name="signer_cert_store_info-structure"></a><span data-ttu-id="060e7-103">\_ \_ \_ Структура сведений о хранилище сертификатов подписывающих</span><span class="sxs-lookup"><span data-stu-id="060e7-103">SIGNER\_CERT\_STORE\_INFO structure</span></span>

<span data-ttu-id="060e7-104">**\_ \_ \_ Информационная структура хранилища сертификатов подписывания** определяет хранилище сертификатов, используемое для подписания документа.</span><span class="sxs-lookup"><span data-stu-id="060e7-104">The **SIGNER\_CERT\_STORE\_INFO** structure specifies the certificate store used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="060e7-105">Эта структура не определена ни в одном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="060e7-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="060e7-106">Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="060e7-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="060e7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="060e7-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a><span data-ttu-id="060e7-108">Члены</span><span class="sxs-lookup"><span data-stu-id="060e7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="060e7-109">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="060e7-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="060e7-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="060e7-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="060e7-111">**псигнингцерт**</span><span class="sxs-lookup"><span data-stu-id="060e7-111">**pSigningCert**</span></span>
</dt> <dd>

<span data-ttu-id="060e7-112">Указатель на структуру [**\_ контекста сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) для сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="060e7-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="060e7-113">**двцертполици**</span><span class="sxs-lookup"><span data-stu-id="060e7-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="060e7-114">Указывает способ добавления сертификатов в сигнатуру.</span><span class="sxs-lookup"><span data-stu-id="060e7-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="060e7-115">Чтобы найти цепочку сертификатов, в дополнение к магазину, указанному членом **хцертсторе** , проверяются хранилища My, CA, root и SPC.</span><span class="sxs-lookup"><span data-stu-id="060e7-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="060e7-116">Этот элемент может иметь одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="060e7-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="060e7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="060e7-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="060e7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="060e7-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="060e7-119"><dt>**\_ Подписавший \_ \_ Цепочка политик сертификатов**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="060e7-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="060e7-120">Добавьте в цепочку сертификатов только сертификаты.</span><span class="sxs-lookup"><span data-stu-id="060e7-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="060e7-121"><dt>**\_ Подписавший \_ \_ Цепочка политик сертификатов \_ без \_ корня**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="060e7-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="060e7-122">Добавляйте в цепочку сертификатов только сертификаты, за исключением корневого сертификата.</span><span class="sxs-lookup"><span data-stu-id="060e7-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="060e7-123"><dt>**\_ Подписавший \_ \_ Хранилище политик сертификатов**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="060e7-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="060e7-124">Добавьте все сертификаты в хранилище, указанное членом **хцертсторе** .</span><span class="sxs-lookup"><span data-stu-id="060e7-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="060e7-125">Этот флаг может быть сочетанием побитового **или** с любым из других возможных значений для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="060e7-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="060e7-126">**хцертсторе**</span><span class="sxs-lookup"><span data-stu-id="060e7-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="060e7-127">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="060e7-127">Optional.</span></span> <span data-ttu-id="060e7-128">Маркер дополнительного хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="060e7-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="060e7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="060e7-129">Requirements</span></span>



| <span data-ttu-id="060e7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="060e7-130">Requirement</span></span> | <span data-ttu-id="060e7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="060e7-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="060e7-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="060e7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="060e7-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="060e7-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="060e7-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="060e7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="060e7-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="060e7-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="060e7-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="060e7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="060e7-137">**сертификат подписи \_**</span><span class="sxs-lookup"><span data-stu-id="060e7-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 




