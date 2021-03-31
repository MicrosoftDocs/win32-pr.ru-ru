---
title: Свойство Item Ивмвиртуалнетворкколлектион (Впккоминтерфацес. h)
description: Объект Ивмвиртуалнетворк, соответствующий указанному индексу.
ms.assetid: 1c6a3449-f76a-4216-8840-0fb9fb133e67
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмвиртуалнетворкколлектион
- Интерфейс Ивмвиртуалнетворкколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Item
- IVMVirtualNetworkCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac5a7648db4708fbc1b445029419ee794809abcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071716"
---
# <a name="ivmvirtualnetworkcollectionitem-property"></a>Свойство Ивмвиртуалнетворкколлектион:: Item

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает объект [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) , соответствующий указанному индексу.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Значение свойства

Объект [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) .

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>                                                      |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр *virtualNetwork* имеет **значение NULL**.<br/>                                        |
| <dl> <dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt> </dl>  | Индекс запрошенного элемента не соответствует элементу в этой коллекции.<br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/>                                                  |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                           |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl>  |
| IID<br/>                      | IID \_ ивмвиртуалнетворкколлектион определен как 8ed680be-4242-4b2a-a21c-1982d8b0f675<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалнетворк**](ivmvirtualnetwork.md)
</dt> <dt>

[**ивмвиртуалнетворкколлектион**](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

