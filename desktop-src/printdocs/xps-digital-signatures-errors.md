---
description: В следующей таблице перечислены все значения HRESULT, которые могут возвращаться методами в API цифровой подписи XPS.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: Ошибки API цифровой подписи XPS (Кспсдигиталсигнатуре. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348212"
---
# <a name="xps-digital-signature-api-errors"></a><span data-ttu-id="519b2-103">Ошибки API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="519b2-103">XPS Digital Signature API Errors</span></span>

<span data-ttu-id="519b2-104">В следующей таблице перечислены все значения **HRESULT** , которые могут возвращаться методами в API цифровой подписи XPS.</span><span class="sxs-lookup"><span data-stu-id="519b2-104">The following table lists all **HRESULT** values that can be returned by the methods in the XPS Digital Signature API.</span></span> <span data-ttu-id="519b2-105">Обратите внимание, что не каждый метод может возвращать все возвращаемые значения, перечисленные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="519b2-105">Note that not every method can return every return value listed in this table.</span></span>



| <span data-ttu-id="519b2-106">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="519b2-106">Return code/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="519b2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="519b2-107">Description</span></span>                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="519b2-108"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="519b2-108"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                                                                                 | <span data-ttu-id="519b2-109">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="519b2-109">The method succeeded.</span></span><br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <span data-ttu-id="519b2-110"><dt>**XPS \_ \_Недопустимый \_ сигнатуреблокк \_ наценка**</dt> <dt>0x8052038b</dt></span><span class="sxs-lookup"><span data-stu-id="519b2-110"><dt>**XPS\_E\_INVALID\_SIGNATUREBLOCK\_MARKUP**</dt> <dt>0x8052038b</dt></span></span> </dl> | <span data-ttu-id="519b2-111">Обнаружена ошибка в XML-разметке блока Signature во время чтения разметки подписи.</span><span class="sxs-lookup"><span data-stu-id="519b2-111">Encountered an error in the XML markup of the signature block while the signature markup was being read.</span></span><br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <span data-ttu-id="519b2-112"><dt>**XPS \_ \_ \_ \_ Элементы совместимости с разметкой E**</dt> <dt>0x80520389</dt></span><span class="sxs-lookup"><span data-stu-id="519b2-112"><dt>**XPS\_E\_MARKUP\_COMPATIBILITY\_ELEMENTS**</dt> <dt>0x80520389</dt></span></span> </dl> | <span data-ttu-id="519b2-113">Значение [**\_ \_ флагов знака XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) указано, что элементы совместимости разметки не ожидались. Однако обнаружены элементы совместимости разметки.</span><span class="sxs-lookup"><span data-stu-id="519b2-113">The [**XPS\_SIGN\_FLAGS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) value specified that no markup compatibility elements were expected; however, markup compatibility elements were found.</span></span><br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <span data-ttu-id="519b2-114"><dt>**XPS \_ E \_ \_ Отсоединенный объект**</dt> <dt>0x8052038a</dt></span><span class="sxs-lookup"><span data-stu-id="519b2-114"><dt>**XPS\_E\_OBJECT\_DETACHED**</dt> <dt>0x8052038a</dt></span></span> </dl>                                            | <span data-ttu-id="519b2-115">Интерфейс не связан с диспетчером сигнатур.</span><span class="sxs-lookup"><span data-stu-id="519b2-115">The interface is not associated with the signature manager.</span></span><br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <span data-ttu-id="519b2-116"><dt>**XPS \_ \_Пакет E \_ уже \_ открыт**</dt> <dt>0x80520387</dt></span><span class="sxs-lookup"><span data-stu-id="519b2-116"><dt>**XPS\_E\_PACKAGE\_ALREADY\_OPENED**</dt> <dt>0x80520387</dt></span></span> </dl>                      | <span data-ttu-id="519b2-117">Пакет XPS уже открыт в диспетчере подписей.</span><span class="sxs-lookup"><span data-stu-id="519b2-117">An XPS package has already been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <span data-ttu-id="519b2-118"><dt>**XPS \_ \_Пакет E \_ не \_ открыт**</dt> <dt>0x80520386</dt></span><span class="sxs-lookup"><span data-stu-id="519b2-118"><dt>**XPS\_E\_PACKAGE\_NOT\_OPENED**</dt> <dt>0x80520386</dt></span></span> </dl>                                  | <span data-ttu-id="519b2-119">Пакет XPS еще не был открыт в диспетчере подписей.</span><span class="sxs-lookup"><span data-stu-id="519b2-119">An XPS package has not yet been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <span data-ttu-id="519b2-120"><dt>**XPS \_ E \_ сигнатуреид \_ DUP**</dt> <dt>0x80520388</dt></span><span class="sxs-lookup"><span data-stu-id="519b2-120"><dt>**XPS\_E\_SIGNATUREID\_DUP**</dt> <dt>0x80520388</dt></span></span> </dl>                                            | <span data-ttu-id="519b2-121">Две или более сигнатур имеют одинаковый идентификатор.</span><span class="sxs-lookup"><span data-stu-id="519b2-121">Two or more signatures have the same ID.</span></span><br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <span data-ttu-id="519b2-122"><dt>**XPS \_ E \_ сигрекуестид \_ DUP**</dt> <dt>0x80520385</dt></span><span class="sxs-lookup"><span data-stu-id="519b2-122"><dt>**XPS\_E\_SIGREQUESTID\_DUP**</dt> <dt>0x80520385</dt></span></span> </dl>                                         | <span data-ttu-id="519b2-123">Идентификатор запроса подписи не уникален в блоке сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="519b2-123">The signature request ID is not unique within the signature block.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="519b2-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="519b2-124">Remarks</span></span>

<span data-ttu-id="519b2-125">Некоторые методы API цифровой подписи XPS выполняют вызовы к API [упаковки](/previous-versions/windows/desktop/opc/packaging) .</span><span class="sxs-lookup"><span data-stu-id="519b2-125">Some XPS digital signature API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="519b2-126">Дополнительные сведения о возвращаемых значениях API упаковки см. в разделе [ошибки упаковки](/previous-versions/windows/desktop/opc/packaging-errors).</span><span class="sxs-lookup"><span data-stu-id="519b2-126">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="519b2-127">Требования</span><span class="sxs-lookup"><span data-stu-id="519b2-127">Requirements</span></span>



| <span data-ttu-id="519b2-128">Требование</span><span class="sxs-lookup"><span data-stu-id="519b2-128">Requirement</span></span> | <span data-ttu-id="519b2-129">Значение</span><span class="sxs-lookup"><span data-stu-id="519b2-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="519b2-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="519b2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="519b2-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="519b2-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="519b2-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="519b2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="519b2-133">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="519b2-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="519b2-134">Header</span><span class="sxs-lookup"><span data-stu-id="519b2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="519b2-135"><dt>Кспсдигиталсигнатуре. h</dt></span><span class="sxs-lookup"><span data-stu-id="519b2-135"><dt>Xpsdigitalsignature.h</dt></span></span> </dl>   |
| <span data-ttu-id="519b2-136">IDL</span><span class="sxs-lookup"><span data-stu-id="519b2-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="519b2-137"><dt>Кспсдигиталсигнатуре. idl</dt></span><span class="sxs-lookup"><span data-stu-id="519b2-137"><dt>XpsDigitalSignature.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="519b2-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="519b2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="519b2-139">Обработка ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="519b2-139">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="519b2-140">Ошибки упаковки</span><span class="sxs-lookup"><span data-stu-id="519b2-140">Packaging Errors</span></span>](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[<span data-ttu-id="519b2-141">Возвращаемые значения криптографии</span><span class="sxs-lookup"><span data-stu-id="519b2-141">Cryptography Return Values</span></span>](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

