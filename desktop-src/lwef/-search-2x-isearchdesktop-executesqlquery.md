---
title: Исеарчдесктоп Ексекутесклкуери, метод
description: Принимает указатель на строку, содержащую запрос язык SQL (SQL) и его атрибуты, и возвращает указатель на возвращаемый набор.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- Устаревшие функции среды Windows в методе Ексекутесклкуери
- Метод Ексекутесклкуери устаревшие функции среды Windows, интерфейс Исеарчдесктоп
- Интерфейс Исеарчдесктоп устаревшие функции среды Windows, метод Ексекутесклкуери
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0b13ff361d07f99efe1366e2201d610eac10523
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "103789156"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>Метод Исеарчдесктоп:: Ексекутесклкуери

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Принимает указатель на строку, содержащую запрос язык SQL (SQL) и его атрибуты, и возвращает указатель на возвращаемый набор.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдваттрибутес* \[ окне\]
</dt> <dd>

Тип: **лпквстр \***

Строка, содержащая другие атрибуты для запроса.

</dd> <dt>

*пвсзурл* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Строка, содержащая SQL-запрос.

</dd> <dt>

*ппидурл* \[ заполняет\]
</dt> <dd>

Тип: **ппидурл \***

При успешном возврате этого метода содержит указатель на возвращенный набор записей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

 

 




