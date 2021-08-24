---
description: Метод «разместить \_ BorderWidth» задает ширину сплошной границы вдоль краев шаблона очистки.
ms.assetid: a618926a-efa4-47a2-9ce9-ae298ed41083
title: 'Идкстжпег: метод ut_BorderWidth:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d5c73121c3a7f4c1db45768fde1d19865648d7ada23ad488f417812471bd9912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697443"
---
# <a name="idxtjpegput_borderwidth-method"></a>Идкстжпег::p \_ метод UT BorderWidth

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_BorderWidth`Метод задает ширину сплошной границы вдоль краев шаблона очистки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_BorderWidth(
  [in] long newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Ширина границы в пикселях.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

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
</dt> </dl>

 

 




