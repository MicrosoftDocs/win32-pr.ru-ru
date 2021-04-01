---
title: Метод IBackgroundCopyManager CreateJob (Deliveryoptimization.h)
description: Создает задание.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Метод CreateJob
- Метод CreateJob, интерфейс Ибаккграундкопиманажер
- Интерфейс Ибаккграундкопиманажер, метод CreateJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/27/2021
ms.locfileid: "104081649"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a>Метод Ибаккграундкопиманажер:: CreateJob

Создает задание.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдисплайнаме* \[ окне\]
</dt> <dd>

Строка, завершающаяся нулем, которая содержит отображаемое имя для задания. Как правило, отображаемое имя используется для распознавания задания в пользовательском интерфейсе. Обратите внимание, что более одного задания могут иметь одно и то же отображаемое имя. Не может иметь **значение NULL**. Длина имени ограничена 256 символами, не включая знак завершения null.

</dd> <dt>

*Тип* \[ окне\]
</dt> <dd>

Тип задания перемещения, например BG_JOB_TYPE_DOWNLOAD. Список типов перемещения см. в разделе Перечисление [**BG_JOB_TYPE**](bg-job-type.md) .

</dd> <dt>

*пжобид* \[ заполняет\]
</dt> <dd>

Уникально идентифицирует задание в очереди. Используйте этот идентификатор при вызове метода [**ибаккграундкопиманажер:: жетжоб**](ibackgroundcopymanager-getjob.md) для получения задания из очереди.

</dd> <dt>

*ппжоб* \[ заполняет\]
</dt> <dd>

Указатель интерфейса [**использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md) , который используется для изменения свойств задания и указания файлов для передачи. Чтобы активировать задание в очереди, вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) . Выпустите *ппжоб* по завершении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения **HRESULT** , а также другие.



| Код возврата                                                                              | Описание                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Новое задание успешно создано.<br/> |



 

## <a name="remarks"></a>Комментарии

Только пользователь, создающий задание или пользователь с правами администратора, может [добавлять файлы в задание](https://www.bing.com/search?q=add+files+to+the+job) и [изменять свойства задания](https://www.bing.com/search?q=change+the+job's+properties).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager определен как 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибаккграундкопиманажер**](ibackgroundcopymanager.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>
