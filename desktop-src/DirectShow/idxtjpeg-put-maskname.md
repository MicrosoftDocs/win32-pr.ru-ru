---
description: '\_Метод маскнаме указывает имя JPEG-файла, используемого в качестве маски очистки.'
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: 'Идкстжпег: метод ut_MaskName:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7a43398020c49f2a6dab1cd56fc0244c4be88e2e45e38e0f6bd63c119bbf66a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755944"
---
# <a name="idxtjpegput_maskname-method"></a>Идкстжпег::p UT \_ маскнаме метод

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_MaskName`Метод задает имя JPEG-файла, используемого в качестве маски очистки. Эта маска будет использоваться вместо одной из встроенных масок очистки. Файл должен содержать монохромный градиент с 8 битами на пиксель. Градиент используется в качестве маски для определения хода выполнения очистки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Указывает имя файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Чтобы вернуться к встроенной маске, установите свойство **маскнум** .

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Идкстжпег**](idxtjpeg.md)
</dt> <dt>

[**Идкстжпег::p UT \_ маскнум**](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




