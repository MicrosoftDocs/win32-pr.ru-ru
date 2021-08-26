---
description: Метод Сеткутпоинт задает время, когда переход переходит от одного источника к другому, если переход визуализируется как вырезание.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'Метод Иамтимелинетранс:: Сеткутпоинт (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c411925ebe10ad35641e38ae2332605d7691ae24f0cc96ff716bd7d00e6603f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052074"
---
# <a name="iamtimelinetranssetcutpoint-method"></a>Метод Иамтимелинетранс:: Сеткутпоинт

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetCutPoint`Метод задает время, когда переход переходит от одного источника к другому, если переход визуализируется как вырезание.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тлтиме* 
</dt> <dd>

Отрезать точку относительно начала перехода, в единицах с 100 нс. Если значение выходит за границы перехода, оно усекается до ближайшего допустимого времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

По умолчанию вырезанная точка является серединой перехода. Например, в переходе, охватывающем одну секунду, вырезанная точка по умолчанию составляет 0,5 секунд в процессе перехода.

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

[**Интерфейс Иамтимелинетранс**](iamtimelinetrans.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




