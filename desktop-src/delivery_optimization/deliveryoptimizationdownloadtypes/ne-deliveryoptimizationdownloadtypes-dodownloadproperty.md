---
title: Перечисление Додовнлоадпроперти
description: Указывает идентификатор свойств для операции скачивания DO.
keywords:
- Перечисление Додовнлоадпроперти, Додовнлоадпроперти
topic_type:
- apiref
api_name:
- DODownloadProperty
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: bb8ec6ad8cc55239522f953c6a81a8bf7b2b62ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137002"
---
# <a name="dodownloadproperty-enumeration"></a>Перечисление Додовнлоадпроперти

Перечисление **додовнлоадпроперти** указывает идентификатор свойств для операции скачивания Do. Это перечисление используется интерфейсом **идодовнлоад** и выполняется с помощью значения типа Variant, где содержится тип значения.

## <a name="syntax"></a>Синтаксис

```cpp
typedef enum _DODownloadProperty
{
  DODownloadProperty_Id = 0,
  DODownloadProperty_Uri,
  DODownloadProperty_ContentId,
  DODownloadProperty_DisplayName,
  DODownloadProperty_LocalPath,
  DODownloadProperty_HttpCustomHeaders,
  DODownloadProperty_CostPolicy,
  DODownloadProperty_SecurityFlags,
  DODownloadProperty_CallbackFreqPercent,
  DODownloadProperty_CallbackFreqSeconds,
  DODownloadProperty_NoProgressTimeoutSeconds,
  DODownloadProperty_ForegroundPriority,
  DODownloadProperty_BlockingMode,
  DODownloadProperty_CallbackInterface,
  DODownloadProperty_StreamInterface,
  DODownloadProperty_SecurityContext,
  DODownloadProperty_NetworkToken
  DODownloadProperty_CorrelationVector,
  DODownloadProperty_DecryptionInfo,
  DODownloadProperty_IntegrityCheckInfo,
  DODownloadProperty_IntegrityCheckMandatory,
  DODownloadProperty_TotalSizeBytes
} DODownloadProperty;
```

## <a name="constants"></a>Константы

| Требование | Значение |
|-|-|
| DODownloadProperty_Id | Только для чтения. Это свойство используется для получения идентификатора, уникально идентифицирующего загрузку. Тип VARIANT — VT_BSTR. |
| DODownloadProperty_Uri | Это свойство используется для задания или получения удаленного пути URI ресурса для скачивания. Это свойство является обязательным, только если не указано *DODownloadProperty_ContentId* . Тип VARIANT — VT_BSTR. |
| DODownloadProperty_ContentId | Это свойство используется для задания или получения уникального идентификатора содержимого для скачивания. Это свойство является обязательным, только если не указано *DODownloadProperty_Uri* . Тип VARIANT — VT_BSTR. |
| DODownloadProperty_DisplayName | Необязательный элемент. Это свойство используется для задания или получения отображаемого имени загрузки. Тип VARIANT — VT_BSTR. |
| DODownloadProperty_LocalPath | Это свойство используется для задания или получения имени локального пути для сохранения файла загрузки. Если путь не существует, то попытается создать его с правами вызывающего. Это свойство является обязательным только в том случае, если *DODownloadProperty_StreamInterface* не было предоставлено. Тип VARIANT — VT_BSTR. |
| DODownloadProperty_HttpCustomHeaders | Необязательный элемент. Это свойство используется для установки или получения настраиваемых заголовков HTTP-запроса. Эти заголовки будут включены во время операций запроса файлов HTTP. Заголовки должны быть уже отформатированы как стандартные заголовки HTTP. Тип VARIANT — VT_BSTR. |
| DODownloadProperty_CostPolicy | Необязательный элемент. Это свойство используется для задания или получения одного из значений перечисления **додовнлоадкостполици** . Тип VARIANT — VT_UI4. |
| DODownloadProperty_SecurityFlags | Необязательный только для записи. Это свойство используется для установки или получения стандартных флагов безопасности WinHTTP (**WINHTTP_OPTION_SECURITY_FLAGS**). Тип VARIANT — VT_UI4.</br></br>Поддерживаются следующие флаги:</br>SECURITY_FLAG_IGNORE_CERT_CN_INVALID. Разрешает недопустимое общее имя в сертификате.</br>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID. Разрешает недействительную дату сертификата.</br>SECURITY_FLAG_IGNORE_UNKNOWN_CA. Разрешает недопустимый центр сертификации.</br>SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE. Позволяет установить удостоверение сервера с помощью сертификата, не являющегося сервером.</br>WINHTTP_ENABLE_SSL_REVOCATION. Разрешает отзыв SSL. Если этот флаг установлен, указанные выше флаги будут пропущены. |
| DODownloadProperty_CallbackFreqPercent | Необязательный элемент. Это свойство используется для задания или получения частоты обратного вызова на основе процента загрузки. Тип VARIANT — VT_UI4. |
| DODownloadProperty_CallbackFreqSeconds | Необязательный элемент. Это свойство используется для задания или получения частоты обратного вызова на основе времени загрузки. Значение по умолчанию — каждые одну секунду. Тип VARIANT — VT_UI4. |
| DODownloadProperty_NoProgressTimeoutSeconds | Необязательный элемент. Используйте это свойство, чтобы задать или получить длину времени ожидания скачивания для отсутствия хода выполнения. Минимальное допустимое значение — 60 секунд для операции скачивания. Тип VARIANT — VT_UI4. |
| DODownloadProperty_ForegroundPriority | Необязательный элемент. Это свойство используется для задания или получения текущего приоритета загрузки. VARIANT_TRUE значение будет загружаться на передний план с более высоким приоритетом. Значение по умолчанию — приоритет фона. Тип VARIANT — VT_BOOL. |
| DODownloadProperty_BlockingMode | Необязательный элемент. Это свойство используется для установки или получения текущего режима блокировки загрузки. VARIANT_TRUE значение приведет к блокированию **идодовнлоад:: Start** для блокировки до завершения скачивания или возникновения ошибки. Значение по умолчанию — неблокируемый режим. Тип VARIANT — VT_BOOL. |
| DODownloadProperty_CallbackInterface | Необязательный элемент. Это свойство используется для установки или получения указателя на интерфейс **идодовнлоадстатускаллбакк** , используемый для обратных вызовов загрузки. Тип VARIANT — VT_UNKNOWN. |
| DODownloadProperty_StreamInterface | Необязательный элемент. Это свойство используется для задания или получения указателя на интерфейс IStream, используемый для типа загрузки потока. Тип VARIANT — VT_UNKNOWN. |
| DODownloadProperty_SecurityContext | Необязательный только для записи. Используйте это свойство, чтобы задать контекст сертификата для использования во время операций запроса HTTP. Значение должно состоять из сериализованных байтов CERT_CONTEXT. Тип VARIANT — (VT_ARRAY \| VT_UI1). |
| DODownloadProperty_NetworkToken | Необязательный только для записи. Это свойство используется для задания сетевого маркера, который будет использоваться во время операций HTTP. VARIANT_TRUE значение приведет к записи маркера удостоверения вызывающего объекта, и VARIANT_FALSE очистит существующий токен. По умолчанию используется маркер вошедшего в систему пользователя. Тип VARIANT — VT_BOOL. |
| DODownloadProperty_CorrelationVector | Необязательный элемент. Задает конкретный вектор корреляции для телеметрии. Тип VARIANT — VT_BSTR. |
| DODownloadProperty_DecryptionInfo | Необязательный только для записи. Задает сведения о расшифровке в виде строки JSON. Тип VARIANT — VT_BSTR. |
| DODownloadProperty_IntegrityCheckInfo | Необязательный только для записи. Задает расположение файлового хэша (ФФ), которое используется, чтобы выполнять проверку целостности во время выполнения для загруженного содержимого. Тип VARIANT — VT_BSTR. |
| DODownloadProperty_IntegrityCheckMandatory | Необязательный элемент. Задает логический флаг, указывающий, является ли использование хэш-файла фрагмента (ФФ) обязательным. Если VARIANT_TRUE, загрузка будет прервана в случае сбоя проверки целостности. Тип VARIANT — VT_BOOL. |
| DODownloadProperty_TotalSizeBytes | Необязательный элемент. Указывает общий размер скачивания в байтах. Тип VARIANT — VT_UI8. |

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Деливерйоптимизатиондовнлоадтипес. h |
