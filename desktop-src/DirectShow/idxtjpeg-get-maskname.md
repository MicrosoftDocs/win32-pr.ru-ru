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
ms.openlocfilehash: d984f426289b9017ca316567b474beaa41b39a35f0ab012ea94ffdd8db33a36b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584744"
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

## <a name="remarks"></a>Remarks

Если переход на очистку использует одну из встроенных SMPTE для очистки, то значением этого свойства является пустая строка.

Вызывающий объект должен освободить возвращенную строку с помощью функции **сисфристринг** .

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Идкстжпег**](idxtjpeg.md)
</dt> <dt>

[**Идкстжпег:: Get \_ маскнум**](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




