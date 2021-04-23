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
# <a name="isearchdesktopexecutesqlquery-method"></a><span data-ttu-id="ee6cb-106">Метод Исеарчдесктоп:: Ексекутесклкуери</span><span class="sxs-lookup"><span data-stu-id="ee6cb-106">ISearchDesktop::ExecuteSQLQuery method</span></span>

> [!NOTE]
> <span data-ttu-id="ee6cb-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ee6cb-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="ee6cb-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="ee6cb-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="ee6cb-109">Принимает указатель на строку, содержащую запрос язык SQL (SQL) и его атрибуты, и возвращает указатель на возвращаемый набор.</span><span class="sxs-lookup"><span data-stu-id="ee6cb-109">Takes a pointer to a string that contains a Structured Query Language (SQL) query and its attributes and returns a pointer to the return set.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee6cb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee6cb-110">Syntax</span></span>


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a><span data-ttu-id="ee6cb-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee6cb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee6cb-112">*пдваттрибутес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee6cb-112">*pdwAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6cb-113">Тип: **лпквстр \***</span><span class="sxs-lookup"><span data-stu-id="ee6cb-113">Type: **LPCWSTR\***</span></span>

<span data-ttu-id="ee6cb-114">Строка, содержащая другие атрибуты для запроса.</span><span class="sxs-lookup"><span data-stu-id="ee6cb-114">A string that contains the other attributes for the query.</span></span>

</dd> <dt>

<span data-ttu-id="ee6cb-115">*пвсзурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee6cb-115">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6cb-116">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="ee6cb-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ee6cb-117">Строка, содержащая SQL-запрос.</span><span class="sxs-lookup"><span data-stu-id="ee6cb-117">A string that contains the SQL query.</span></span>

</dd> <dt>

<span data-ttu-id="ee6cb-118">*ппидурл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ee6cb-118">*ppidUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6cb-119">Тип: **ппидурл \***</span><span class="sxs-lookup"><span data-stu-id="ee6cb-119">Type: **ppidUrl\***</span></span>

<span data-ttu-id="ee6cb-120">При успешном возврате этого метода содержит указатель на возвращенный набор записей.</span><span class="sxs-lookup"><span data-stu-id="ee6cb-120">When this method returns successfully, contains a pointer to the returned recordset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee6cb-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee6cb-121">Return value</span></span>

<span data-ttu-id="ee6cb-122">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ee6cb-122">Type: **HRESULT**</span></span>

<span data-ttu-id="ee6cb-123">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ee6cb-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ee6cb-124">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee6cb-124">Otherwise, it returns an **HRESULT** error code.</span></span>

 

 




