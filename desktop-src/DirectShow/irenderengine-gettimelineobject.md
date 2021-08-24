---
description: Метод Жеттимелинеобжект извлекает временную шкалу, используемую подсистемой рендеринга в данный момент.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: 'Метод Ирендеренгине:: Жеттимелинеобжект (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c21868dc705a5c9f3b40649540fcaadb1f9219a7443d58c59964606cb7ed7d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823364"
---
# <a name="irenderenginegettimelineobject-method"></a>Метод Ирендеренгине:: Жеттимелинеобжект

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetTimelineObject`Метод получает временную шкалу, используемую в настоящий момент подсистемой отрисовки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пптимелине* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**иамтимелине**](iamtimeline.md) временной шкалы. Если шкала времени отсутствует, она получает значение **null** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** :



| Код возврата                                                                                            | Описание                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                   | Успешно.<br/>                            |
| <dl> <dt>**\_указатель E**</dt> </dl>              | Недопустимый указатель.<br/>                    |
| <dl> <dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt> </dl> | Не удалось инициализировать модуль визуализации.<br/> |



 

## <a name="remarks"></a>Remarks

При возврате, если значение *\* Пптимелине* не **равно NULL**, то интерфейс **иамтимелине** имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

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

[**Интерфейс Ирендеренгине**](irenderengine.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




