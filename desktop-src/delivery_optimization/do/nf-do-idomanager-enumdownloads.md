---
title: 'Метод Идоманажер:: Енумдовнлоадс'
description: Извлекает указатель интерфейса на объект перечислителя, используемый для перечисления существующих Скачиваний.
keywords:
- 'Метод Идоманажер:: Енумдовнлоадс'
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5442196b95e654755b4f84fe85375afb8f5b9372ddae453ca4ddffb567882fda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543831"
---
# <a name="idomanagerenumdownloads-method"></a>Метод Идоманажер:: Енумдовнлоадс

Извлекает указатель интерфейса на объект перечислителя, используемый для перечисления существующих Скачиваний.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a>Параметры

`category`

Необязательный параметр. Имя свойства, используемое в качестве категории для перечисления. При передаче `nullptr` будут получены все существующие файлы для загрузки. В качестве категории поддерживаются следующие свойства.

- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`ppEnum`

Адрес указателя интерфейса на **иенумункновн**, который используется для перечисления существующих Скачиваний. Содержимое перечислителя зависит от значения *Category*. Загружаемые файлы, включенные в интерфейс перечисления, — это те, которые ранее были созданы тем же вызывающим объектом для этой функции. 

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
