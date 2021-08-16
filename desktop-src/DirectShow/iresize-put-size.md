---
description: Метод помещения \_ размера задает размер выходных данных и режим Stretch.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: 'Иресизе: метод ut_Size:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d2da95cca7bf19182dd4c0f5f385715256ae9c5253c356094110c028fb1b016d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818134"
---
# <a name="iresizeput_size-method"></a>Иресизе: метод:p UT \_ size

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_Size`Метод задает размер выходных данных и режим Stretch.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Высота* \[ окне\]
</dt> <dd>

Высота видео в пикселях.

</dd> <dt>

*Ширина* \[ окне\]
</dt> <dd>

Ширина видео в пикселях.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Режим Stretch. Возможные значения см. в разделе [**изменение размера флагов**](resize-flags.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

DES может вызывать этот метод до или после вызова метода **размещения \_ mediaType**. Если DES вызывает этот метод перед вызовом метода OUTPUT **\_ mediaType**, фильтр должен выбрать значение по умолчанию для битовой глубины и использовать значения размера для создания выходного типа носителя. Если DES вызывает этот метод после вызова метода OUTPUT **\_ mediaType**, фильтр должен изменить его текущий тип вывода на новые размеры.

DES может также вызывать этот метод после подключения выходного контакта. В этом случае измените тип выходных данных и повторно подключите выходной ПИН-код к новому типу. Дополнительные сведения см. в разделе [Повторное подключение ПИН](reconnecting-pins.md) -кодов.

Параметр *flags* указывает, как фильтр должен выполнить операцию изменения размера.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | DirectX 9,0 или более поздней версии<br/>                                                         |
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> <dt>

[**Интерфейс Иресизе**](iresize.md)
</dt> </dl>

 

 




