---
title: Свойство Item Ивмнетворкадаптерколлектион (Впккоминтерфацес. h)
description: Объект Ивмнетворкадаптер, соответствующий указанному индексу.
ms.assetid: 3de76e24-3315-473f-870b-074be8bcfe70
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмнетворкадаптерколлектион
- Интерфейс Ивмнетворкадаптерколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Item
- IVMNetworkAdapterCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1c84eb28eb0af583fd18db21ef13c9345caf6c03838d0b11c2af0a80e164bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973972"
---
# <a name="ivmnetworkadaptercollectionitem-property"></a>Свойство Ивмнетворкадаптерколлектион:: Item

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает объект [**ивмнетворкадаптер**](ivmnetworkadapter.md) , соответствующий указанному индексу.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMNetworkAdapter **networkInterface
);
```



## <a name="property-value"></a>Значение свойства

Объект [**ивмнетворкадаптер**](ivmnetworkadapter.md) .

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно. <br/>                                                      |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр *networkInterface* имеет **значение NULL**. <br/>                                      |
| <dl> <dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt> </dl>  | Индекс запрошенного элемента не соответствует элементу в этой коллекции. <br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/>                                                   |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                           |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                  |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl>  |
| IID<br/>                      | IID \_ ивмнетворкадаптерколлектион определен как ebaeafe9-EBCD-47cf-866e-ad87d735e479<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмнетворкадаптер**](ivmnetworkadapter.md)
</dt> <dt>

[**ивмнетворкадаптерколлектион**](ivmnetworkadaptercollection.md)
</dt> </dl>

 

