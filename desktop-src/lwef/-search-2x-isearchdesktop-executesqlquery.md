---
title: Исеарчдесктоп Ексекутесклкуери, метод
description: принимает указатель на строку, содержащую запрос язык SQL (SQL) и его атрибуты и возвращает указатель на возвращаемый набор.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- устаревшие функции Windows метода ексекутесклкуери
- устаревшие функции Windows метода ексекутесклкуери, интерфейс исеарчдесктоп
- устаревшие функции Windows интерфейса исеарчдесктоп, метод ексекутесклкуери
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec436a427958988e7605673b12b3fd8dc6fd3e1a54ab61cc5f542f0494c34923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014294"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>Метод Исеарчдесктоп:: Ексекутесклкуери

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

принимает указатель на строку, содержащую запрос язык SQL (SQL) и его атрибуты и возвращает указатель на возвращаемый набор.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
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

строка, содержащая запрос SQL.

</dd> <dt>

*ппидурл* \[ заполняет\]
</dt> <dd>

Тип: **ппидурл \***

При успешном возврате этого метода содержит указатель на возвращенный набор записей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

 

 




