---
title: Метод Ивмпстрингколлектион Item
description: Метод Item возвращает строку по указанному индексу.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- проигрыватель Windows Media метода элемента
- метод Item проигрыватель Windows Media, интерфейс ивмпстрингколлектион
- проигрыватель Windows Media интерфейса ивмпстрингколлектион, метод Item
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47928502dce9ed4deb12461763a499de5d962aa1303b4c9cc5eacb02c7619da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568431"
---
# <a name="iwmpstringcollectionitem-method"></a>Метод Ивмпстрингколлектион:: Item

Метод **Item** возвращает строку по указанному индексу.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*Линдекс* \[ окне\]
</dt> <dd>

Объект **System. Int32** , который является индексом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Строка **System. String** , которая является строкой по указанному индексу.

## <a name="remarks"></a>Remarks

Интерфейс **ивмпстрингколлектион** используется для получения набора значений, доступных для атрибута. Например, метод **ивмпмедиаколлектион. жетаттрибутестрингколлектион** можно использовать для получения интерфейса **ивмпстрингколлектион** , представляющего все значения атрибута жанра в типе носителя Audio. Затем метод **Item** можно использовать для итерации всех возможных значений атрибута жанра.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ивмпмедиаколлектион. Жетаттрибутестрингколлектион (VB и C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Медиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпстрингколлектион (VB и C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





