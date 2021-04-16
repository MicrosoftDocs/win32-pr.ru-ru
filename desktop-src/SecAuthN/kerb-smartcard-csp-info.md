---
description: Содержит сведения о поставщике служб шифрования (CSP) смарт-карты.
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: Структура KERB_SMARTCARD_CSP_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 03b1a8084e291dde5a4f1f2017e4e97f57640bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650841"
---
# <a name="kerb_smartcard_csp_info-structure"></a><span data-ttu-id="abee6-103">\_ \_ Информационная структура CSP Kerberos для смарт-карт \_</span><span class="sxs-lookup"><span data-stu-id="abee6-103">KERB\_SMARTCARD\_CSP\_INFO structure</span></span>

<span data-ttu-id="abee6-104">Структура **\_ сведений о \_ CSP \_** для смарт-карты Kerberos содержит сведения о [*поставщике служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="abee6-104">The **KERB\_SMARTCARD\_CSP\_INFO** structure contains information about a smart card [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="abee6-105">Эта структура не объявлена в общедоступном заголовке.</span><span class="sxs-lookup"><span data-stu-id="abee6-105">This structure is not declared in a public header.</span></span>

## <a name="syntax"></a><span data-ttu-id="abee6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abee6-106">Syntax</span></span>


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a><span data-ttu-id="abee6-107">Члены</span><span class="sxs-lookup"><span data-stu-id="abee6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="abee6-108">**двкспинфолен**</span><span class="sxs-lookup"><span data-stu-id="abee6-108">**dwCspInfoLen**</span></span>
</dt> <dd>

<span data-ttu-id="abee6-109">Размер (в байтах) этой структуры, включая все добавленные данные.</span><span class="sxs-lookup"><span data-stu-id="abee6-109">The size, in bytes, of this structure, including any appended data.</span></span>

</dd> <dt>

<span data-ttu-id="abee6-110">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="abee6-110">**MessageType**</span></span>
</dt> <dd>

<span data-ttu-id="abee6-111">Тип передаваемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="abee6-111">The type of message being passed.</span></span> <span data-ttu-id="abee6-112">Этот элемент должен иметь значение 1.</span><span class="sxs-lookup"><span data-stu-id="abee6-112">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="abee6-113">**контекстинформатион**</span><span class="sxs-lookup"><span data-stu-id="abee6-113">**ContextInformation**</span></span>
</dt> <dd>

<span data-ttu-id="abee6-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="abee6-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="abee6-115">**SpaceHolderForWow64**</span><span class="sxs-lookup"><span data-stu-id="abee6-115">**SpaceHolderForWow64**</span></span>
</dt> <dd>

<span data-ttu-id="abee6-116">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="abee6-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="abee6-117">**flags**</span><span class="sxs-lookup"><span data-stu-id="abee6-117">**flags**</span></span>
</dt> <dd>

<span data-ttu-id="abee6-118">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="abee6-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="abee6-119">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="abee6-119">**KeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="abee6-120">Закрытый ключ для использования из контейнера ключей, указанного в буфере **ббуффер**.</span><span class="sxs-lookup"><span data-stu-id="abee6-120">The private key to use from the key container specified within the buffer **bBuffer**.</span></span> <span data-ttu-id="abee6-121">Ключ может принимать одно из следующих значений, определенных в Винкрипт. h.</span><span class="sxs-lookup"><span data-stu-id="abee6-121">The key can be one of the following values, defined in WinCrypt.h.</span></span>



| <span data-ttu-id="abee6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="abee6-122">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="abee6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="abee6-123">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="abee6-124"><dt>**В \_ КЭЙЕКСЧАНЖЕ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="abee6-124"><dt>**AT\_KEYEXCHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="abee6-125">Ключ является ключом обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="abee6-125">The key is a key-exchange key.</span></span><br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="abee6-126"><dt>**В \_ ПОДПИСЬ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="abee6-126"><dt>**AT\_SIGNATURE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="abee6-127">Ключ является ключом подписи.</span><span class="sxs-lookup"><span data-stu-id="abee6-127">The key is a signature key.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="abee6-128">**нкарднамеоффсет**</span><span class="sxs-lookup"><span data-stu-id="abee6-128">**nCardNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="abee6-129">Число символов в буфере **ббуффер** , предшествующее имени смарт-карты в этом буфере.</span><span class="sxs-lookup"><span data-stu-id="abee6-129">The number of characters in the **bBuffer** buffer that precede the name of the smart card in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="abee6-130">Если имя смарт-карты не указано, буфер должен содержать пустую строку.</span><span class="sxs-lookup"><span data-stu-id="abee6-130">If the name of the smart card is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="abee6-131">**нреадернамеоффсет**</span><span class="sxs-lookup"><span data-stu-id="abee6-131">**nReaderNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="abee6-132">Число символов в буфере **ббуффер** , предшествующее имени считывателя смарт-карт в этом буфере.</span><span class="sxs-lookup"><span data-stu-id="abee6-132">The number of characters in the **bBuffer** buffer that precede the name of the smart card reader in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="abee6-133">Если имя считывателя смарт-карт не указано, буфер должен содержать пустую строку.</span><span class="sxs-lookup"><span data-stu-id="abee6-133">If the name of the smart card reader is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="abee6-134">**нконтаинернамеоффсет**</span><span class="sxs-lookup"><span data-stu-id="abee6-134">**nContainerNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="abee6-135">Число символов в буфере **ббуффер** , предшествующее имени контейнера ключей в этом буфере.</span><span class="sxs-lookup"><span data-stu-id="abee6-135">The number of characters in the **bBuffer** buffer that precede the name of the key container in that buffer.</span></span> <span data-ttu-id="abee6-136">Эта строка не может быть пустой.</span><span class="sxs-lookup"><span data-stu-id="abee6-136">This string cannot be empty.</span></span>

</dd> <dt>

<span data-ttu-id="abee6-137">**нкспнамеоффсет**</span><span class="sxs-lookup"><span data-stu-id="abee6-137">**nCSPNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="abee6-138">Число символов в буфере **ббуффер** , предшествующее имени CSP в этом буфере.</span><span class="sxs-lookup"><span data-stu-id="abee6-138">The number of characters in the **bBuffer** buffer that precede the name of the CSP in that buffer.</span></span>

</dd> <dt>

<span data-ttu-id="abee6-139">**ббуффер**</span><span class="sxs-lookup"><span data-stu-id="abee6-139">**bBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="abee6-140">Массив символов, инициализированных длиной `sizeof(DWORD)` .</span><span class="sxs-lookup"><span data-stu-id="abee6-140">An array of characters initialized to a length of `sizeof(DWORD)`.</span></span> <span data-ttu-id="abee6-141">Этот буфер содержит имена, на которые ссылаются члены **нкарднамеоффсет**, **нреадернамеоффсет**, **нконтаинернамеоффсет** и **нкспнамеоффсет** , а также любые дополнительные данные, предоставляемые CSP.</span><span class="sxs-lookup"><span data-stu-id="abee6-141">This buffer contains the names referred to by the **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset**, and **nCSPNameOffset** members, as well as any additional data provided by the CSP.</span></span>

<span data-ttu-id="abee6-142">Все имена, которые не предоставляются, должны быть представлены в этом буфере пустыми строками.</span><span class="sxs-lookup"><span data-stu-id="abee6-142">Any names that are not provided must be represented in this buffer by empty strings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abee6-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abee6-143">Remarks</span></span>

<span data-ttu-id="abee6-144">При сериализации этой структуры члены структуры должны быть согласованы с границами, кратными 2 байтам.</span><span class="sxs-lookup"><span data-stu-id="abee6-144">When this structure is serialized, the structure members must be aligned to boundaries that are multiples of 2 bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="abee6-145">Требования</span><span class="sxs-lookup"><span data-stu-id="abee6-145">Requirements</span></span>



| <span data-ttu-id="abee6-146">Требование</span><span class="sxs-lookup"><span data-stu-id="abee6-146">Requirement</span></span> | <span data-ttu-id="abee6-147">Значение</span><span class="sxs-lookup"><span data-stu-id="abee6-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="abee6-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abee6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="abee6-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abee6-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="abee6-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abee6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="abee6-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="abee6-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="abee6-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abee6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abee6-153">**\_Вход с сертификатом Kerberos \_**</span><span class="sxs-lookup"><span data-stu-id="abee6-153">**KERB\_CERTIFICATE\_LOGON**</span></span>](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
