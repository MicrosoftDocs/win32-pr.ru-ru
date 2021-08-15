---
description: Следующие константы используются с протоколом сертифицированной защиты выходных данных (Копп) для конкретных механизмов защиты выходных данных.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: Флаги типа защиты Копп (Дксва. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 75038b22a30be41389311fd1a7cfb830f870859b01ba48fd9a791a42cee86dc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119214054"
---
# <a name="copp-protection-type-flags"></a>Флаги типа защиты Копп

Следующие константы используются с протоколом сертифицированной защиты выходных данных (Копп) для конкретных механизмов защиты выходных данных.



| Константа/значение                                                                                                                                                                                                                                                                                                             | Описание                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <dt>**Копп \_ ProtectionType \_ неизвестный**</dt> <dt>0x80000000</dt> </dl>     | Неизвестный механизм защиты.<br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <dt>**Копп \_ ProtectionType \_ нет**</dt> , <dt>0x00000000</dt> </dl>                 | Нет механизмов защиты.<br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <dt>**Копп \_ ProtectionType \_ HDCP**</dt> <dt>0x00000001</dt> </dl>                 | High-Bandwidth цифровой Защита содержимого (HDCP).<br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <dt>**Копп \_ ProtectionType \_ ACP**</dt> , <dt>0x00000002</dt> </dl>                     | Аналоговая защита от копирования (ACP).<br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <dt>**Копп \_ ProtectionType \_ кгмса**</dt> <dt>0x00000004</dt> </dl>             | Аналоговая система управления копиями (CGMS-A).<br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <dt>**Копп \_ 0x80000007 \_ Mask ProtectionType**</dt> <dt></dt> </dl>                 | Битовая маска для изоляции допустимых флагов.<br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <dt>**Копп \_ ProtectionType \_ зарезервированный**</dt> <dt>0x7FFFFFF8</dt> </dl> | Зарезервировано. Должен равняться нулю.<br/>                              |



## <a name="remarks"></a>Remarks

Некоторые методы возвращают один флаг из этого типа перечисления, а некоторые методы возвращают побитовую операцию **или** для одного или нескольких флагов.

Эти флаги используются в следующих запросах и командах Копп.

-   Глобальный уровень защиты
-   Локальный уровень защиты
-   Тип защиты
-   Задать уровень защиты

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Дксва. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы и идентификаторы GUID](constants-and-guids.md)
</dt> <dt>

[Использование протокола сертифицированной выходной защиты (Копп)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




