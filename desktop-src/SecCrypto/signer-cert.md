---
description: Указывает сертификат, используемый для подписания документа. Сертификат может храниться в файле сертификата издателя программного обеспечения (SPC) или в хранилище сертификатов.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: Структура SIGNER_CERT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266098"
---
# <a name="signer_cert-structure"></a><span data-ttu-id="e07ee-104">\_Структура сертификата подписывающий</span><span class="sxs-lookup"><span data-stu-id="e07ee-104">SIGNER\_CERT structure</span></span>

<span data-ttu-id="e07ee-105">Структура **\_ сертификата подписи** определяет [*сертификат*](../secgloss/c-gly.md) , используемый для подписания документа.</span><span class="sxs-lookup"><span data-stu-id="e07ee-105">The **SIGNER\_CERT** structure specifies a [*certificate*](../secgloss/c-gly.md) used to sign a document.</span></span> <span data-ttu-id="e07ee-106">Сертификат может храниться в файле [*сертификата издателя программного обеспечения*](../secgloss/s-gly.md) (SPC) или в [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e07ee-106">The certificate can be stored in a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) file or in a [*certificate store*](../secgloss/c-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="e07ee-107">Эта структура не определена ни в одном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="e07ee-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="e07ee-108">Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="e07ee-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e07ee-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e07ee-109">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a><span data-ttu-id="e07ee-110">Члены</span><span class="sxs-lookup"><span data-stu-id="e07ee-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e07ee-111">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="e07ee-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="e07ee-112">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="e07ee-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="e07ee-113">**двцертчоице**</span><span class="sxs-lookup"><span data-stu-id="e07ee-113">**dwCertChoice**</span></span>
</dt> <dd>

<span data-ttu-id="e07ee-114">Указывает способ хранения сертификата.</span><span class="sxs-lookup"><span data-stu-id="e07ee-114">Specifies how the certificate is stored.</span></span> <span data-ttu-id="e07ee-115">Этот элемент может иметь одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e07ee-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="e07ee-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e07ee-116">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="e07ee-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e07ee-117">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <span data-ttu-id="e07ee-118"><dt>**\_ Подписавший СЕРТИФИКАТ \_ SPC \_ файл**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e07ee-118"><dt>**SIGNER\_CERT\_SPC\_FILE**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="e07ee-119">Сертификат хранится в файле SPC.</span><span class="sxs-lookup"><span data-stu-id="e07ee-119">The certificate is stored in an SPC file.</span></span> <span data-ttu-id="e07ee-120">Член **пвсзспкфиле** содержит путь и имя файла SPC.</span><span class="sxs-lookup"><span data-stu-id="e07ee-120">The **pwszSpcFile** member contains the path and file name of the SPC file.</span></span><br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <span data-ttu-id="e07ee-121"><dt>**\_ Подписавший \_Хранилище сертификатов**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e07ee-121"><dt>**SIGNER\_CERT\_STORE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="e07ee-122">Сертификат хранится в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="e07ee-122">The certificate is stored in a certificate store.</span></span> <span data-ttu-id="e07ee-123">Элемент **пцертстореинфо** содержит указатель на [**\_ \_ \_ информационную структуру хранилища сертификатов подписавший**](signer-cert-store-info.md) , указывающий хранилище сертификатов, в котором хранится сертификат.</span><span class="sxs-lookup"><span data-stu-id="e07ee-123">The **pCertStoreInfo** member contains a pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span><br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <span data-ttu-id="e07ee-124"><dt>**\_ Подписавший \_ \_ Цепочка сертификатов SPC**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e07ee-124"><dt>**SIGNER\_CERT\_SPC\_CHAIN**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e07ee-125">Сертификат хранится в файле SPC и связывается с цепочкой сертификатов.</span><span class="sxs-lookup"><span data-stu-id="e07ee-125">The certificate is stored in an SPC file and is associated with a certificate chain.</span></span> <span data-ttu-id="e07ee-126">Элемент **пспкчаининфо** содержит указатель на структуру [**\_ \_ \_ сведений о цепочке SPC**](signer-spc-chain-info.md) , которая содержит сведения о цепочке для сертификата.</span><span class="sxs-lookup"><span data-stu-id="e07ee-126">The **pSpcChainInfo** member contains a pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e07ee-127">**пвсзспкфиле**</span><span class="sxs-lookup"><span data-stu-id="e07ee-127">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="e07ee-128">Указатель на строку в Юникоде, заканчивающуюся нулем и содержащую путь и имя файла SPC, в котором хранится сертификат.</span><span class="sxs-lookup"><span data-stu-id="e07ee-128">A pointer to a null-terminated Unicode string that contains the path and file name of the SPC file in which the certificate is stored.</span></span> <span data-ttu-id="e07ee-129">Этот элемент используется только в том случае, если член **двцертчоице** содержит **SPC- \_ \_ \_ файл сертификата подписывающий**.</span><span class="sxs-lookup"><span data-stu-id="e07ee-129">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_FILE**.</span></span>

</dd> <dt>

<span data-ttu-id="e07ee-130">**пцертстореинфо**</span><span class="sxs-lookup"><span data-stu-id="e07ee-130">**pCertStoreInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e07ee-131">Указатель на [**\_ \_ \_ информационную структуру хранилища сертификатов подписывающих**](signer-cert-store-info.md) , указывающий хранилище сертификатов, в котором хранится сертификат.</span><span class="sxs-lookup"><span data-stu-id="e07ee-131">A pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span> <span data-ttu-id="e07ee-132">Этот элемент используется только в том случае, если элемент **двцертчоице** содержит **\_ \_ хранилище сертификатов подписывающих**.</span><span class="sxs-lookup"><span data-stu-id="e07ee-132">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_STORE**.</span></span>

</dd> <dt>

<span data-ttu-id="e07ee-133">**пспкчаининфо**</span><span class="sxs-lookup"><span data-stu-id="e07ee-133">**pSpcChainInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e07ee-134">Указатель на структуру [**\_ \_ \_ сведений о цепочке SPC**](signer-spc-chain-info.md) , которая содержит сведения о цепочке для сертификата.</span><span class="sxs-lookup"><span data-stu-id="e07ee-134">A pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span> <span data-ttu-id="e07ee-135">Этот элемент используется только в том случае, если элемент **двцертчоице** содержит **\_ \_ \_ цепочку сертификатов SPC**.</span><span class="sxs-lookup"><span data-stu-id="e07ee-135">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_CHAIN**.</span></span>

</dd> <dt>

<span data-ttu-id="e07ee-136">**HWND**</span><span class="sxs-lookup"><span data-stu-id="e07ee-136">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="e07ee-137">Маркер окна, используемый в качестве владельца всех отображаемых диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="e07ee-137">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="e07ee-138">Этот элемент в настоящее время не используется и не учитывается.</span><span class="sxs-lookup"><span data-stu-id="e07ee-138">This member is not currently used and is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e07ee-139">Требования</span><span class="sxs-lookup"><span data-stu-id="e07ee-139">Requirements</span></span>



| <span data-ttu-id="e07ee-140">Требование</span><span class="sxs-lookup"><span data-stu-id="e07ee-140">Requirement</span></span> | <span data-ttu-id="e07ee-141">Значение</span><span class="sxs-lookup"><span data-stu-id="e07ee-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e07ee-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e07ee-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e07ee-143">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e07ee-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e07ee-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e07ee-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e07ee-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e07ee-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e07ee-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e07ee-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07ee-147">**сигнерсигн**</span><span class="sxs-lookup"><span data-stu-id="e07ee-147">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="e07ee-148">**сигнерсигнекс**</span><span class="sxs-lookup"><span data-stu-id="e07ee-148">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
