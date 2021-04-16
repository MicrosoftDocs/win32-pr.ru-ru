---
description: Метод NOLOCK Извлекает состояние редактирования объекта (заблокировано или разблокировано).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'Метод Иамтимелинеобж:: NOLOCK (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679666"
---
# <a name="iamtimelineobjgetlocked-method"></a>Метод Иамтимелинеобж:: NOLOCK

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetLocked`Метод получает состояние редактирования объекта (заблокировано или разблокировано). Заблокированное состояние указывает, что объект не должен редактироваться; незаблокированное состояние указывает, что объект можно изменять. Временная шкала не обеспечивает принудительную блокировку. Параметр блокировки существует только для удобства приложения.

## <a name="syntax"></a>Синтаксис


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pVal* 
</dt> <dd>

Получает состояние редактирования объекта. Если значение равно **true**, объект заблокирован и не должен редактироваться. Если **значение равно false**, объект разблокируется и может быть изменен.

</dd> </dl>

## <a name="remarks"></a>Комментарии

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

 

 




