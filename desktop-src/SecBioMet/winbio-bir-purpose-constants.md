---
title: Константы WINBIO_BIR_PURPOSE (Винбио \_ types. h)
description: Укажите цель, для которой предназначена запись биометрической информации (Бир) или для которой она подходит.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988711"
---
# <a name="winbio_bir_purpose-constants"></a>\_ \_ Константы назначения Бир винбио

Следующие флаги используются членом **назначения** структуры [**\_ \_ заголовков винбио Бир**](winbio-bir-header.md) для указания цели, для которой предназначена запись биометрической информации (Бир) или для которой она подходит.



| Константа                                                                                                                                                                                                                                          | Описание                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <dt>**ВИНБИО \_ нет \_ \_ доступных целей**</dt> </dl>                                         | Назначение не указано.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <dt>**\_Проверка цели \_ винбио**</dt> </dl>                                                            | Проверьте удостоверение пользователя.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <dt>**\_назначение винбио \_**</dt> </dl>                                                      | Определяет пользователя.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <dt>**\_Регистрация цели \_ винбио**</dt> </dl>                                                            | Регистрация пользователя.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <dt>**ВИНБИО \_ цель \_ регистрации \_ для \_ проверки**</dt> </dl>       | Запишите образец биометрической метрики и определите, соответствует ли образец указанному удостоверению пользователя.<br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <dt>**\_Регистрация назначения \_ винбио \_ для \_ идентификации**</dt> </dl> | Запишите образец биометрической метрики и определите, соответствует ли он существующему биометрической шаблону.<br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <dt>**\_Аудит назначения \_ винбио**</dt> </dl>                                                               | Дополнительные сведения, которые можно использовать для ведения журнала или для вывода. Это значение игнорируется на входе всеми функциями. На выходе он будет доступен только в том случае, если он поддерживается биометрической единицей, и вы указали **\_ флаг данных винбио \_ \_ RAW** в параметре *flags* функции [**винбиокаптуресампле**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) .<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> <dt>

[**\_заголовок винбио Бир \_**](winbio-bir-header.md)
</dt> </dl>

 

 





