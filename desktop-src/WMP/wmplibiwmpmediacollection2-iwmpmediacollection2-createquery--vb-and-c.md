---
title: IWMPMediaCollection2 createQuery, метод
description: Метод createQuery возвращает интерфейс Ивмпкуери, представляющий новый запрос.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- проигрыватель Windows Media метода createQuery
- проигрыватель Windows Media метода createQuery, интерфейс IWMPMediaCollection2
- проигрыватель Windows Media интерфейса IWMPMediaCollection2, метод createQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1644748008e2b222fef0101a96892d480ad4723b9892b94e0e69c387b54e53d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000094"
---
# <a name="iwmpmediacollection2createquery-method"></a>Метод IWMPMediaCollection2:: createQuery

`createQuery`Метод возвращает интерфейс **ивмпкуери** , представляющий новый запрос.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмпкуери** , представляющий новый пустой запрос.

## <a name="remarks"></a>Remarks

Создание нового запроса — это первый шаг к созданию составного запроса.

## <a name="examples"></a>Примеры

В следующем примере используется `createQuery` для получения интерфейса **ивмпкуери** , который инициализируется значением NULL. Так как для этого запроса не было добавлено никаких условий, при его использовании в качестве аргумента в методе **жетстрингколлектионбикуери** метод возвращает коллекцию строк, содержащую все элементы мультимедиа указанного типа мультимедиа. Затем Коллекция строк отображается в списке.


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс IWMPMediaCollection2 (VB и C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпкуери (VB и C#)**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





