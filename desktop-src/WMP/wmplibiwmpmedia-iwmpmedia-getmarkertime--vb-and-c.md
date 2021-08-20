---
title: Ивмпмедиа Жетмаркертиме, метод
description: Метод Жетмаркертиме Возвращает время маркера по указанному индексу.
ms.assetid: 1c617e3a-0978-479c-a636-b655082232c1
keywords:
- проигрыватель Windows Media метода жетмаркертиме
- проигрыватель Windows Media метода жетмаркертиме, интерфейс ивмпмедиа
- проигрыватель Windows Media интерфейса ивмпмедиа, метод жетмаркертиме
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293ad08137df1b87f47f614781d92be2b7c310fa7282cc234b38e1f3e0e63586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115699"
---
# <a name="iwmpmediagetmarkertime-method"></a>Метод Ивмпмедиа:: Жетмаркертиме

Метод **жетмаркертиме** Возвращает время маркера по указанному индексу.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Double getMarkerTime(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerTime( _
  ByVal MarkerNum As System.Int32 _
) As System.Double
Implements IWMPMedia.getMarkerTime
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*Маркернум* \[ окне\]
</dt> <dd>

Объект **System. Int32** , который является индексом маркера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Double** , которое является временем метки.

## <a name="remarks"></a>Remarks

Этот метод возвращает **значение NULL** , если указанный маркер не существует.

Некоторые элементы мультимедиа не содержат маркеров. Используйте **маркеркаунт** , чтобы узнать, сколько маркеров находится в текущем элементе мультимедиа.

Номера индексов маркеров начинаются с 1.

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере кода используется **жетмаркертиме** для заполнения многострочного текстового поля с расположением каждого маркера. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker times.
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker information in the array.
        markers[i] = "Marker number " + i + " occurs at ";
        markers[i] += player.currentMedia.getMarkerTime(i).ToString();
        markers[i] += " second(s).";
    }

    // Display the marker times in the text box.
    markerTimes.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker times.
Dim markers(mcount) As String

&#39; Verify that at least one marker exists in the current media.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker information in the array.
        markers(i) = (&quot;Marker number &quot; + i + &quot; occurs at &quot;)
        markers(i) += player.currentMedia.getMarkerTime(i).ToString()
        markers(i) += &quot; second(s).&quot;

    Next i

    &#39; Display the marker times in the text box.
    markerTimes.Lines = markers

End If
```





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Маркеркаунт (VB и C#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





