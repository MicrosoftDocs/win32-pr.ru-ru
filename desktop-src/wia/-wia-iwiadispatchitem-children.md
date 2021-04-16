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
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719367"
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

## <a name="remarks"></a>Комментарии

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




