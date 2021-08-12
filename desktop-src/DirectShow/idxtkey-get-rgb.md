---
description: Метод Get \_ RGB извлекает цвет RGB для ключа. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB.
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: 'Метод Идксткэй:: get_RGB (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 596595e38ce57b026631d1ba7bd88d501bc50661ea3034fecd9ad4fbd9615428
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652413"
---
# <a name="idxtkeyget_rgb-method"></a>Метод Идксткэй:: Get \_ RGB

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_RGB`Метод извлекает цвет RGB, по которому следует подключаться. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Pval* \[ out, retval\]
</dt> <dd>

Получает цвет. Возвращаемое значение представляет собой шестнадцатеричное число в формате 0xRRGGBB, где RR — это значение красного цвета, а параметр GG — зеленое значение, а BB — синий.

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

[**Идксткэй:: Get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




