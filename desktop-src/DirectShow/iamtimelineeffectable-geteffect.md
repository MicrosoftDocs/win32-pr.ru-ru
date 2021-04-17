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
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680069"
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



 

## <a name="remarks"></a>Комментарии

Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс **иамтимелинеобж** имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелиниффектабле**](iamtimelineeffectable.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




