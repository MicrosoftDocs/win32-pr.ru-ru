---
title: Перечисление Додовнлоадпропертекс
description: Указывает идентификатор расширенных свойств для операции "выполнить скачивание".
keywords:
- Перечисление Додовнлоадпропертекс, Додовнлоадпропертекс
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: f5ec26d845fd6df2bfe0e84fffed0979c39e1971244788c9dfe5ddd3a0c0beca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990384"
---
# <a name="dodownloadpropertyex-enumeration"></a>Перечисление Додовнлоадпропертекс

> [!IMPORTANT]
> Перечисление **додовнлоадпропертекс** является устаревшим. Вместо этого используйте перечисление [додовнлоадпроперти](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) с [идодовнлоад::](../do/nf-do-idodownload-getproperty.md) и [идодовнлоад:: SetProperty](../do/nf-do-idodownload-setproperty.md).

Перечисление **додовнлоадпропертекс** указывает идентификатор расширенных свойств для операции скачивания Do. Это перечисление используется интерфейсом **идодовнлоадинтернал** , а значение **типа Variant** используется для получения и задания значения свойства.

## <a name="syntax"></a>Синтаксис

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a>Константы

| Требование | Значение |
|-|-|
| DODownloadPropertyEx_UpdateId | Зарезервировано. Не используется. |
| DODownloadPropertyEx_CorrelationVector | Необязательный элемент. Задает конкретный вектор корреляции для телеметрии. Тип VARIANT — VT_BSTR. |
| DODownloadPropertyEx_DecryptionInfo | Зарезервировано. Не используется. |
| DODownloadPropertyEx_IntegrityCheckInfo | Необязательный только для записи. Задает расположение файлового хэша (ФФ), которое используется, чтобы выполнять проверку целостности во время выполнения для загруженного содержимого. Тип VARIANT — VT_BSTR. |
| DODownloadPropertyEx_IntegrityCheckMandatory | Необязательный элемент. Задает логический флаг, указывающий, является ли использование хэш-файла фрагмента (ФФ) обязательным. Если VARIANT_TRUE, загрузка будет прервана после сбоя проверки целостности. Тип VARIANT — VT_BOOL. |
| DODownloadPropertyEx_TotalSizeBytes | Зарезервировано. Не используется. |
| DODownloadPropertyEx_TempLocalFileUsage | Зарезервировано. Не используется. |

## <a name="requirements"></a>Requirements (Требования)

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Додовнлоадинтернал. h |
