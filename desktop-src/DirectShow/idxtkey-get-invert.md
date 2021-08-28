---
description: '\_Метод инверсии получает логическое значение, указывающее, выполняется ли обратная операция с ключом. Это свойство применяется ко всем типам ключей, за исключением ДКСТКЭЙ \_ Alpha.'
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'Метод Идксткэй:: get_Invert (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c5a862e062175d3c052a5003a2ced60fe5d3cc439bff76315e046fc2153f73af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083854"
---
# <a name="idxtkeyget_invert-method"></a>Метод Идксткэй:: Get \_ инверсия

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_Invert`Метод получает логическое значение, указывающее, выполняется ли обратная операция с ключом. Это свойство применяется ко всем типам ключей, за исключением ДКСТКЭЙ \_ Alpha.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Pval* \[ out, retval\]
</dt> <dd>

Получает одно из следующих значений.



| Значение     | Описание                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| **TRUE**  | Пикселы в перевернутом изображении инвертированы по отношению к операции по умолчанию. |
| **FALSE** | Пикселы в изображении с чрезмерной назначением становятся прозрачными по умолчанию.         |



 

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

[**Интерфейс Идксткэй**](idxtkey.md)
</dt> <dt>

[**Идксткэй:: Get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




