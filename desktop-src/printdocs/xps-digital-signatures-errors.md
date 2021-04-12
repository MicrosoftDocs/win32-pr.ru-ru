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
# <a name="xps-digital-signature-api-errors"></a>Ошибки API цифровой подписи XPS

В следующей таблице перечислены все значения **HRESULT** , которые могут возвращаться методами в API цифровой подписи XPS. Обратите внимание, что не каждый метод может возвращать все возвращаемые значения, перечисленные в этой таблице.



| Возвращаемый код и значение                                                                                                                                                                                                                                                                                  | Описание                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**\_ОК**</dt> </dl>                                                                                                                                                                 | Метод выполнен успешно.<br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <dt>**XPS \_ \_Недопустимый \_ сигнатуреблокк \_ наценка**</dt> <dt>0x8052038b</dt> </dl> | Обнаружена ошибка в XML-разметке блока Signature во время чтения разметки подписи.<br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <dt>**XPS \_ \_ \_ \_ Элементы совместимости с разметкой E**</dt> <dt>0x80520389</dt> </dl> | Значение [**\_ \_ флагов знака XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) указано, что элементы совместимости разметки не ожидались. Однако обнаружены элементы совместимости разметки.<br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <dt>**XPS \_ E \_ \_ Отсоединенный объект**</dt> <dt>0x8052038a</dt> </dl>                                            | Интерфейс не связан с диспетчером сигнатур.<br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <dt>**XPS \_ \_Пакет E \_ уже \_ открыт**</dt> <dt>0x80520387</dt> </dl>                      | Пакет XPS уже открыт в диспетчере подписей. <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <dt>**XPS \_ \_Пакет E \_ не \_ открыт**</dt> <dt>0x80520386</dt> </dl>                                  | Пакет XPS еще не был открыт в диспетчере подписей. <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <dt>**XPS \_ E \_ сигнатуреид \_ DUP**</dt> <dt>0x80520388</dt> </dl>                                            | Две или более сигнатур имеют одинаковый идентификатор.<br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <dt>**XPS \_ E \_ сигрекуестид \_ DUP**</dt> <dt>0x80520385</dt> </dl>                                         | Идентификатор запроса подписи не уникален в блоке сигнатуры.<br/>                                                                                                     |



 

## <a name="remarks"></a>Комментарии

Некоторые методы API цифровой подписи XPS выполняют вызовы к API [упаковки](/previous-versions/windows/desktop/opc/packaging) . Дополнительные сведения о возвращаемых значениях API упаковки см. в разделе [ошибки упаковки](/previous-versions/windows/desktop/opc/packaging-errors).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                            |
| Header<br/>                   | <dl> <dt>Кспсдигиталсигнатуре. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Кспсдигиталсигнатуре. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обработка ошибок в COM](../com/error-handling-in-com.md)
</dt> <dt>

[Ошибки упаковки](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[Возвращаемые значения криптографии](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

