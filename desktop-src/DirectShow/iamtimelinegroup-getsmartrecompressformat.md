---
description: Метод Жетсмартрекомпрессформат извлекает текущий формат сжатия для интеллектуального повторного сжатия.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'Метод Иамтимелинеграуп:: Жетсмартрекомпрессформат (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8560bb9d8da6904cf74b62ffd238b234e9c74ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688907"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a>Метод Иамтимелинеграуп:: Жетсмартрекомпрессформат

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetSmartRecompressFormat`Метод получает текущий формат сжатия для интеллектуального повторного сжатия.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппформат* 
</dt> <dd>

Получает указатель на структуру [**SCompFmt0**](scompfmt0.md) , приводится как указатель на тип long. Если метод завершается с ошибкой, ему присваивается значение **null**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Если в приложении не задан формат интеллектуального сжатия (путем вызова [**иамтимелинеграуп:: сетсмартрекомпрессформат**](iamtimelinegroup-setsmartrecompressformat.md)), то формат, возвращаемый этим методом, будет недопустимым. Вызовите метод [**иамтимелинеграуп:: иссмартрекомпрессформатсет**](iamtimelinegroup-issmartrecompressformatset.md) , чтобы определить, был ли задан формат сжатия.

Если метод завершился с ошибкой, вызывающий объект должен освободить возвращенный тип мультимедиа и удалить структуру [**SCompFmt0**](scompfmt0.md) :


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелинеграуп**](iamtimelinegroup.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




