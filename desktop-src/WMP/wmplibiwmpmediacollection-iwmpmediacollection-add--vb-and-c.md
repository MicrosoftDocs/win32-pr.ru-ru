---
title: Ивмпмедиаколлектион Add, метод
description: Метод Add добавляет новый элемент мультимедиа или список воспроизведения в библиотеку. | Ивмпмедиаколлектион Add, метод
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- добавить проигрыватель Windows Media метода
- добавление проигрыватель Windows Media метода, интерфейс ивмпмедиаколлектион
- проигрыватель Windows Media интерфейса ивмпмедиаколлектион, add, метод
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 778850da4094d8ac745018b115248de9008d15339b7ffee75de177cf957d3fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861170"
---
# <a name="iwmpmediacollectionadd-method"></a>Метод Ивмпмедиаколлектион:: Add

Метод **Add** добавляет новый элемент мультимедиа или список воспроизведения в библиотеку.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бструрл* \[ окне\]
</dt> <dd>

**Строка System. String** , которая представляет собой URL-адрес, указывающий расположение элемента мультимедиа или списка воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмпмедиа** для добавленного элемента или списка воспроизведения.

## <a name="remarks"></a>Remarks

Этот метод загружает существующий элемент мультимедиа или список воспроизведения в библиотеку по заданному пути. Этот метод не перемещает и не изменяет файл. Этот метод завершается ошибкой, если задан недопустимый локальный путь, но сами элементы мультимедиа не проверяются на допустимость перед добавлением в библиотеку.

Этот метод принимает как статические, так и автоматические файлы списков воспроизведения. Метод **ивмпплайлистколлектион. импортплайлист** также можно использовать для добавления статического списка воспроизведения в библиотеку.

Перед вызовом этого метода необходимо иметь полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

в следующем примере в коллекцию носителей проигрыватель Windows Media добавляются три объекта мультимедиа. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
```





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиаколлектион. Remove (VB и C#)**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистколлектион. Импортплайлист (VB и C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





