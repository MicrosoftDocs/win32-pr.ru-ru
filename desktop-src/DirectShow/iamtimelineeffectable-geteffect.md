---
description: Метод "Effect" получает результат на указанном уровне приоритета.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'Метод Иамтимелиниффектабле:: Effect (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d53ecc7c3d5291ddb6b894b24835eeb236f036e94eb166383da907a9f469c960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905184"
---
# <a name="iamtimelineeffectablegeteffect-method"></a>Метод Иамтимелиниффектабле:: Effect

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Метод " **Effect** " получает результат на указанном уровне приоритета.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппфкс* \[ заполняет\]
</dt> <dd>

Получает интерфейс [**иамтимелинеобж**](iamtimelineobj.md) воздействия.

</dd> <dt>

*Какую* 
</dt> <dd>

Уровень приоритета получаемого результата.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение HRESULT. Возможные значения:



| Код возврата                                                                               | Описание                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Не влияет на заданный приоритет,<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>      | Успешно.<br/>                             |
| <dl> <dt>**\_указатель E**</dt> </dl> | **Пустой** аргумент указателя.<br/>           |



 

## <a name="remarks"></a>Remarks

Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс **иамтимелинеобж** имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

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

[**Интерфейс Иамтимелиниффектабле**](iamtimelineeffectable.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




