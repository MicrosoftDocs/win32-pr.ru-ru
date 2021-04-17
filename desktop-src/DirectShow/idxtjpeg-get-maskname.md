---
description: Метод Get \_ маскнаме извлекает имя JPEG-файла, который будет использоваться в качестве маски очистки.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'Метод Идкстжпег:: get_MaskName (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a00c8104ee19cac33a00ff9062006338a19e283b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675118"
---
# <a name="idxtjpegget_maskname-method"></a>Метод Идкстжпег:: Get \_ маскнаме

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_MaskName`Метод получает имя JPEG-файла, который будет использоваться в качестве маски очистки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Pval* \[ out, retval\]
</dt> <dd>

Получает имя файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Если переход на очистку использует одну из встроенных SMPTE для очистки, то значением этого свойства является пустая строка.

Вызывающий объект должен освободить возвращенную строку с помощью функции **сисфристринг** .

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

[**Интерфейс Идкстжпег**](idxtjpeg.md)
</dt> <dt>

[**Идкстжпег:: Get \_ маскнум**](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




