---
description: Метод Жетвтракк извлекает виртуальную дорожку по указанному приоритету.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: 'Метод Иамтимелинекомп:: Жетвтракк (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 245f19783f7a472f86544d14f27c588e7a5938e899f2f389887d7a7817d6254e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756304"
---
# <a name="iamtimelinecompgetvtrack-method"></a>Метод Иамтимелинекомп:: Жетвтракк

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetVTrack`Метод извлекает виртуальную дорожку по указанному приоритету.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппвиртуалтракк* \[ заполняет\]
</dt> <dd>

Получает интерфейс [**иамтимелинеобж**](iamtimelineobj.md) виртуальной записи.

</dd> <dt>

*Какую* 
</dt> <dd>

Приоритет извлекаемой виртуальной записи.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** :



| Код возврата                                                                                  | Описание                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Успешно.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Отсутствует виртуальная дорожка с указанным приоритетом.<br/> |
| <dl> <dt>**\_указатель E**</dt> </dl>    | **Пустой** аргумент указателя.<br/>                    |



 

## <a name="remarks"></a>Remarks

Если метод завершается успешно, интерфейс **иамтимелинеобж** , который он возвращает, имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

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

[**Интерфейс Иамтимелинекомп**](iamtimelinecomp.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




