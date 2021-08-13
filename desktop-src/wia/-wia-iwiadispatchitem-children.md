---
description: Свойство Children объекта Item извлекает коллекцию объектов Item. Элементы в этой коллекции представляют элементы, которые являются прямыми дочерними элементами данного элемента в иерархическом дереве. Только для чтения.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Свойство Item. Children
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 72ce5119a10adc6a902d5a675d3ec116a3db1852a88e47ed852284cf44edf2f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440733"
---
# <a name="itemchildren-property"></a>Свойство Item. Children

Свойство **Children** объекта [**Item**](-wia-item.md) извлекает коллекцию объектов **Item** . Элементы в этой коллекции представляют элементы, которые являются прямыми дочерними элементами данного элемента в иерархическом дереве. Только для чтения.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Item.Children
```



## <a name="property-value"></a>Значение свойства

Переменная, которая получает объекты.

## <a name="remarks"></a>Remarks

Это свойство используется для навигации по иерархическому дереву объектов [**элементов**](-wia-item.md) , представляющих устройство, папки и файлы, которые находятся на устройстве.

Свойство **Children** — это коллекция объектов [**элементов**](-wia-item.md) только из уровня, расположенного непосредственно под этим объектом **Item** в дереве. Чтобы перейти к более подробному уровню вниз по дереву, используйте это свойство рекурсивно.

Если элемент не может или не имеет дочерних элементов, это свойство возвращает пустую коллекцию.

> [!Note]  
> Эта коллекция основана на 0.

 

## <a name="examples"></a>Примеры

В следующем примере показано использование свойства **Children** для извлечения и перечисления коллекции дочерних элементов устройства. Если устройство является цифровой камерой, коллекция обычно содержит элементы папки и изображения. Если устройство является сканером, коллекция обычно содержит элементы, представляющие сканирование кроватях.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




