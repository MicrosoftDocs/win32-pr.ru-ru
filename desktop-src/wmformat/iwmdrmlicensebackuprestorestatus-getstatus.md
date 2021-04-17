---
title: Метод Ивмдрмлиценсебаккупресторестатус-Status (Вмдрмсдк. h)
description: Метод WebMethod получает подробные сведения о состоянии операции резервного копирования или восстановления лицензий.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- Метод WebMethod формат Windows Media Format
- Метод WebMethod формат Windows Media Format, интерфейс Ивмдрмлиценсебаккупресторестатус
- Интерфейс Ивмдрмлиценсебаккупресторестатус интерфейса Windows Media Format, методического состояния
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708522"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a>Метод Ивмдрмлиценсебаккупресторестатус:: with Status

Метод WebMethod получает подробные сведения **о состоянии операции** резервного копирования или восстановления лицензий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстатус* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**\_ \_ \_ состояния восстановления резервной копии WM**](wm-backup-restore-status.md) , которая получает сведения о состоянии.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вмдрмсдк. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Вмдрмсдк. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрмлиценсебаккупресторестатус**](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





