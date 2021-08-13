---
title: IDeliveryOptimizationJob2 AddFile, метод
description: Метод AddFile добавляет один файл к существующему заданию DO.
keywords:
- AddFile - метод
- Метод AddFile, интерфейс IDeliveryOptimizationJob2
- Интерфейс IDeliveryOptimizationJob2, метод AddFile
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6d27bca855bb9c719b485060fabf1f10b7130bd864569e74f98516ca76b8fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544639"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a>Метод IDeliveryOptimizationJob2:: Аддфилевисранжес

Метод AddFile добавляет один файл к существующему заданию DO.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*ИД* \[ для окне\]
</dt> <dd>

Строка идентификатора файла, однозначно определяющая загружаемый файл.

</dd> <dt>

*ремотеурл* \[ окне\]
</dt> <dd>

URL-адрес файла, который выполняет попытку подключения для скачивания файла.

</dd> <dt>

*ранжекаунт* \[ окне\]
</dt> <dd>

Количество элементов, содержащихся в *диапазонах*. Нулевое значение означает, что для файла не используются диапазоны.

</dd> <dt>

*диапазоны* \[ окне\]
</dt> <dd>

Необязательный список диапазонов. Каждый диапазон в списке является структурой [**BG_FILE_RANGE**](bg-file-range.md) .

</dd> <dt>

*riid* \[ окне\]
</dt> <dd>

Тип объекта, содержащегося в объекте. Он должен иметь тип IID_IDeliveryOptimizationFile.

</dd> <dt>

*объект* \[ заполняет\]
</dt> <dd>

Объект Иделиверйоптимизатионфиле, представляющий загружаемый файл. 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает S_OK при успешном или одном из стандартных значений HRESULT при ошибке.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|---------------------------|---------------------------------------------------------------------------------|
| Минимальная версия клиента  | Windows 10, только для \[ настольных приложений версии 1803\]                                  |
| Минимальная версия сервера  | Windows Server, только для \[ настольных приложений версии 1709\]                              |
| Header                    | Deliveryoptimization. h                                                          |
| IDL                       | DeliveryOptimization. idl                                                        |
| Библиотека                   | Досвк. lib                                                                       |
| DLL                       | Dosvc.dll                                                                       |
| IID                       | IID_IDeliveryOptimizationJob определяется как EE2584CF-A69C-4848-B633-2649962B3EF7 |

## <a name="see-also"></a>См. также раздел

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
