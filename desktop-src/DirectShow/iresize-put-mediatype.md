---
description: Метод размещения \_ mediaType задает тип выходного носителя для фильтра изменения размера.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: 'Иресизе: метод ut_MediaType:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6c26878af6f091efd3c3f321cb073ce51a8e6236d4bafa326ab99f85f39e1a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818205"
---
# <a name="iresizeput_mediatype-method"></a>Иресизе: метод:p UT \_ mediaType

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_MediaType`Метод задает тип выходного носителя для фильтра изменения размера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*платежная плата* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , содержащую тип носителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Алгоритм DES вызывает этот метод перед подключением выходного ПИН-кода фильтра. Используйте тип носителя в качестве типа носителя выходного контакта. Верните этот тип мультимедиа в метод [**ктрансформфилтер:: жетмедиатипе**](ctransformfilter-getmediatype.md) и проверьте агсинт этот тип в методе [**Ктрансформфилтер:: чекктрансформ**](ctransformfilter-checktransform.md) . DES никогда не вызывает этот метод после подключения выходного контакта.

В настоящее время DES всегда устанавливает тип выходного носителя в несжатый формат RGB с помощью блока формата **видеоинфохеадер** (тип формата равен Format \_ видеоинфо). Подтипом может быть МЕДИАСУБТИПЕ \_ ARGB32, который указывает 32-битный RGB с каналом альфа.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | DirectX 9,0 или более поздней версии<br/>                                                         |
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> <dt>

[**Интерфейс Иресизе**](iresize.md)
</dt> </dl>

 

 




