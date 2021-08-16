---
description: Метод «разместить \_ инверсию» указывает, выполняется ли обратная операция с ключом. Это свойство применяется ко всем типам ключей, за исключением ДКСТКЭЙ \_ Alpha.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: 'Идксткэй: метод ut_Invert:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed1ed445e7a6f5f1f07eff74ac739934f2c9ca1358affe3e0cd699b7a101f0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819441"
---
# <a name="idxtkeyput_invert-method"></a>Идксткэй::p \_ метод инвертора UT

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_Invert`Метод указывает, выполняется ли обратная операция с ключом. Это свойство применяется ко всем типам ключей, за исключением ДКСТКЭЙ \_ Alpha.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Задает логическое значение. **Значение true** показывает, что Пиксели в перевернутом изображении инвертированы по отношению к операции по умолчанию. Если **значение равно false**, Пиксели в изображении с чрезмерной назначением становятся прозрачными по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

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

[**Интерфейс Идксткэй**](idxtkey.md)
</dt> <dt>

[**Идксткэй::p UT \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




