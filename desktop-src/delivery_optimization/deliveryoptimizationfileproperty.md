---
title: Перечисление Деливерйоптимизатионфилепроперти (Deliveryoptimization. h)
description: Перечисление Деливерйоптимизатионфилепроперти указывает идентификатор необязательного свойства для файла DO.
keywords:
- Перечисление Деливерйоптимизатионфилепроперти
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710485"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a>Перечисление Деливерйоптимизатионфилепроперти

Перечисление Деливерйоптимизатионфилепроперти указывает идентификатор необязательного свойства для файла DO. Это перечисление используется в интерфейсе IDeliveryOptimizationFile2, где передается значение свойства типа VARIANT.

## <a name="syntax"></a>Синтаксис

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a>Константы

<dl> <dt>

DOFilePropertyId_DecryptionInfo
</dt> <dd>

Идентификатор свойства DOFilePropertyId_DecryptionInfo задает сведения о расшифровке в виде строки JSON. DOFilePropertyId_DecryptionInfo является свойством только для записи типа VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckInfo
</dt> <dd>

Идентификатор свойства DOFilePropertyId_IntegrityCheckInfo задает расположение файлового хэша (ФФ), которое используется, чтобы выполнять проверку целостности во время выполнения для загруженного содержимого. DOFilePropertyId_IntegrityCheckInfo является свойством только для записи типа VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckMandatory
</dt> <dd>

Идентификатор свойства DOFilePropertyId_IntegrityCheckMandatory задает логический флаг, указывающий, является ли использование ФФ обязательным. Если значение — TRUE, загрузка будет прервана после сбоя проверки целостности. DOFilePropertyId_IntegrityCheckMandatory является свойством для чтения и записи типа VT_BOOL.

</dd> <dt>

DOFilePropertyId_DownloadSinkFilePath
</dt> <dd>

Идентификатор свойства DOFilePropertyId_DownloadSinkFilePath задает полное расположение файловой системы, где следует хранить загруженные фрагменты. DOFilePropertyId_DownloadSinkFilePath имеет тип VT_BSTR.

</dd> <dt>

DOFilePropertyId_DownloadSinkMemoryStream
</dt> <dd>

Идентификатор свойства DOFilePropertyId_DownloadSinkMemoryStream является устаревшим. Не используйте.

</dd> <dt>

DOFilePropertyId_TotalSizeBytes
</dt> <dd>

Идентификатор свойства DOFilePropertyId_TotalSizeBytes указывает общий размер загрузки. DOFilePropertyId_TotalSizeBytes имеет тип VT_UI8.
</dd> </dl>

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------|----------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1803\]<br/>      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>  |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
