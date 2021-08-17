---
description: Метод Жетаутпутбуфферинг Извлекает число кадров, отображаемых заранее во время просмотра.
ms.assetid: 93cb8d18-f1b7-48f9-af41-97f010304b05
title: 'Метод Иамтимелинеграуп:: Жетаутпутбуфферинг (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 52917e798dcc71526f225fbca01038ee11c36c3c65fa1cebda88883ad2ae530e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428494"
---
# <a name="iamtimelinegroupgetoutputbuffering-method"></a>Метод Иамтимелинеграуп:: Жетаутпутбуфферинг

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetOutputBuffering`Метод получает число кадров, отображаемых заранее во время просмотра.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetOutputBuffering(
  [out] int *pnBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнбуффер* \[ заполняет\]
</dt> <dd>

Получает число кадров в буфере.

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

[**Интерфейс Иамтимелинеграуп**](iamtimelinegroup.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




