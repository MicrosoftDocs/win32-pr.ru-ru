---
title: Функция Мрмкреатересаурцефиле (Мрмресаурцеиндексер. h)
description: Создает PRI-файл (с именем \ 0034; Resources. PRI \ 0034;) или файлы на диске в указанной папке. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Меню функций Мрмкреатересаурцефиле и другие ресурсы
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80294e5829dbf90c8aa3b0f6485c2da4185add1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803448"
---
# <a name="mrmcreateresourcefile-function"></a>Функция Мрмкреатересаурцефиле

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Создает PRI-файл (с именем Resources. PRI) или файлы на диске в указанной папке. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индексатор* \[ окне\]
</dt> <dd>

Тип: **[ **мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md)**

Маркер, идентифицирующий индексатор ресурсов, из которого создается PRI-файл.

</dd> <dt>

*паккагингмоде* \[ окне\]
</dt> <dd>

Тип: **[ **мрмпаккагингмоде**](mrmpackagingmode.md)**

Указывает, должен ли PRI-файл быть автономным, автоматически разделяться по квалификатору ресурса или быть пакетом ресурсов.

</dd> <dt>

*паккагингоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **мрмпаккагингоптионс**](mrmpackagingoptions.md)**

Указывает дополнительные параметры для PRI файла.

</dd> <dt>

*outputDirectory* 
</dt> <dd>

Тип: **пквстр**

Путь к папке, в которой будет сохранен PRI-файл.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

\_ОК, если функция прошла успешно, в противном случае — другое значение. Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1803\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только классические приложения Windows Server\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Мрмресаурцеиндексер. h</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мрмсуппорт. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

