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
ms.openlocfilehash: ba7042069d4f1190a88b25ea4cc349e8230c149dd61d2d06fc91fa3439a9e55f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074637"
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

## <a name="remarks"></a>Remarks

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
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




