---
title: Свойство Item Ивмхарддискконнектионколлектион (Впккоминтерфацес. h)
description: Извлекает объект подключения к жесткому диску, соответствующий указанному индексу.
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмхарддискконнектионколлектион
- Интерфейс Ивмхарддискконнектионколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c829d7294925b7f95f8229779ca91e04ce305125d787acad14c8dd7cd9cff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974314"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a>Свойство Ивмхарддискконнектионколлектион:: Item

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает объект подключения к жесткому диску, соответствующий указанному индексу.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a>Значение свойства

Объект [**ивмхарддискконнектион**](ivmharddiskconnection.md) .

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно. <br/>                                                      |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр *харддискконнектион* имеет **значение NULL**. <br/>                                    |
| <dl> <dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt> </dl>  | Индекс запрошенного элемента не соответствует элементу в этой коллекции. <br/> |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl> | Конфигурация неизвестна.<br/>                                                       |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/>                                                   |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                         |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                          |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                               |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                      |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl>      |
| IID<br/>                      | IID \_ ивмхарддискконнектионколлектион определен как b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмхарддискконнектион**](ivmharddiskconnection.md)
</dt> <dt>

[**ивмхарддискконнектионколлектион**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

