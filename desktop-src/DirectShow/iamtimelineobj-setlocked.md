---
description: Метод Сетлоккед устанавливает состояние редактирования объекта как "заблокировано" или "Разблокировано".
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'Метод Иамтимелинеобж:: Сетлоккед (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8707aa86b651553dde2f9f9b57c84169a9969b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676041"
---
# <a name="iamtimelineobjsetlocked-method"></a>Метод Иамтимелинеобж:: Сетлоккед

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetLocked`Метод устанавливает состояние редактирования объекта как "заблокировано" или "Разблокировано".

Заблокированное состояние указывает, что объект не должен редактироваться; незаблокированное состояние указывает, что объект можно изменять. Временная шкала не обеспечивает принудительную блокировку. Параметр блокировки существует только для удобства приложения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* 
</dt> <dd>

Логическое значение, указывающее состояние редактирования объекта. Если **значение — true**, объект заблокирован и не должен редактироваться. Если **значение равно false**, объект разблокируется и может быть изменен.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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

 

 




