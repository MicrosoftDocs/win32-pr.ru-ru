---
description: Метод Жетклассвиндовстилес извлекает стили окон и стили окна.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Кбасевиндов. Жетклассвиндовстилес, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a34332f84a91ee88d61ee5f29f0b6a0b0cc44714
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675476"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a>Кбасевиндов. Жетклассвиндовстилес, метод

`GetClassWindowStyles`Метод получает стили окна и стили окна.

## <a name="syntax"></a>Синтаксис


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пклассстилес* 
</dt> <dd>

Указатель на переменную, которая получает стили класса.

</dd> <dt>

*пвиндовстилес* 
</dt> <dd>

Указатель на переменную, которая получает стили окна.

</dd> <dt>

*пвиндовстилесекс* 
</dt> <dd>

Указатель на переменную, которая получает расширенные стили окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает статическую текстовую строку, содержащую имя класса.

## <a name="remarks"></a>Комментарии

Метод [**кбасевиндов::P репаревиндов**](cbasewindow-preparewindow.md) вызывает этот метод, чтобы получить стили окна и стили окон.

Этот метод является чисто виртуальным; производный класс должен реализовать его. В следующем примере показана возможная реализация:


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



Объект использует стиль класса для элемента **лпсзкласснаме** структуры вндкласс, который передается функции **registerClass** . Объект использует стили окна для параметров *двексстиле* и *двстиле* функции **CreateWindowEx** . Дополнительные сведения см. в разделе пакет SDK для платформы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




