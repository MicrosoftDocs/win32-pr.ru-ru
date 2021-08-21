---
description: Метод Жетнекствтракк извлекает следующую виртуальную запись после указанной виртуальной записи.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'Метод Иамтимелинекомп:: Жетнекствтракк (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dbeaf5d7987f1baf2b3df9804c4abd3049c38042a29f4177f83abec6855140a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401055"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a>Метод Иамтимелинекомп:: Жетнекствтракк

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetNextVTrack`Метод извлекает следующую виртуальную запись после указанной виртуальной записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвиртуалтракк* 
</dt> <dd>

Указатель на предыдущую виртуальную дорожку или **значение NULL** , чтобы получить первую виртуальную дорожку в композиции.

</dd> <dt>

*ппнекствиртуалтракк* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) следующей виртуальной записи в порядке приоритета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК, если метод получает виртуальную дорожку, или \_ false в противном случае.

## <a name="remarks"></a>Remarks

Если метод завершается успешно, интерфейс **иамтимелинеобж** , который он возвращает, имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

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

[**Интерфейс Иамтимелинекомп**](iamtimelinecomp.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




