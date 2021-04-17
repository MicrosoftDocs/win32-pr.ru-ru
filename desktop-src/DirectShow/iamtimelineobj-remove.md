---
description: Метод reinsert удаляет этот объект из временной шкалы (включая подобъекты, но не дочерние элементы) для повторной вставки в других местах.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'Метод Иамтимелинеобж:: Remove (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a3559787dfdacc68130dcaef073f32d07d4a0df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689151"
---
# <a name="iamtimelineobjremove-method"></a>Метод Иамтимелинеобж:: Remove

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`Remove`Метод удаляет этот объект из временной шкалы (включая подобъекты, но не дочерние элементы) для повторной вставки в других местах.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Remove();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод следует вызывать только в том случае, если приложение немедленно вставит объект обратно на временную шкалу. Недопустимая операция для вызова этого метода без повторной вставки объекта. Чтобы окончательно удалить объект, вызовите [**иамтимелинеобж:: RemoveAll**](iamtimelineobj-removeall.md).

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

[**Интерфейс Иамтимелинеобж**](iamtimelineobj.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




