---
description: Освобождает маркер, связанный с последним использованным списком (MRU), и записывает кэшированные данные в реестр.
title: Функция Фримрулист
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 7d31d261629853c3b82b9d1564c5e8755e047570
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840625"
---
# <a name="freemrulist-function"></a><span data-ttu-id="a0e2c-103">Функция Фримрулист</span><span class="sxs-lookup"><span data-stu-id="a0e2c-103">FreeMRUList function</span></span>

<span data-ttu-id="a0e2c-104">Освобождает маркер, связанный с последним использованным списком (MRU), и записывает кэшированные данные в реестр.</span><span class="sxs-lookup"><span data-stu-id="a0e2c-104">Frees the handle associated with the most recently used (MRU) list and writes cached data to the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e2c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0e2c-105">Syntax</span></span>


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a><span data-ttu-id="a0e2c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0e2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0e2c-107">*хмру* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0e2c-107">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e2c-108">Тип: **Handle**</span><span class="sxs-lookup"><span data-stu-id="a0e2c-108">Type: **HANDLE**</span></span>

<span data-ttu-id="a0e2c-109">Маркер списка MRU, который нужно освободить.</span><span class="sxs-lookup"><span data-stu-id="a0e2c-109">The handle of the MRU list to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0e2c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0e2c-110">Return value</span></span>

<span data-ttu-id="a0e2c-111">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="a0e2c-111">Type: **int**</span></span>

<span data-ttu-id="a0e2c-112">При успешном выполнении возвращает неотрицательное значение – 1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a0e2c-112">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0e2c-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="a0e2c-113">Remarks</span></span>

<span data-ttu-id="a0e2c-114">Если список MRU был создан с помощью флага **\_ качеврите MRU** , вызов **фримрулист** приводит к тому, что все изменения, еще не ЗАПИСАНные в версию списка MRU, хранящегося в реестре, будут записаны в данный момент.</span><span class="sxs-lookup"><span data-stu-id="a0e2c-114">If the MRU list was created using the **MRU\_CACHEWRITE** flag, calling **FreeMRUList** causes any changes not yet written to the version of the MRU list stored in registry to be written at this time.</span></span>

<span data-ttu-id="a0e2c-115">Эта функция не включена в общедоступный заголовок или библиотеку.</span><span class="sxs-lookup"><span data-stu-id="a0e2c-115">This function is not included in a public header or library.</span></span> <span data-ttu-id="a0e2c-116">Его необходимо извлечь из comctl32.dll с порядковым номером 152.</span><span class="sxs-lookup"><span data-stu-id="a0e2c-116">It must be extracted from comctl32.dll by ordinal 152.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0e2c-117">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="a0e2c-117">Requirements</span></span>



| <span data-ttu-id="a0e2c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a0e2c-118">Requirement</span></span> | <span data-ttu-id="a0e2c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e2c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e2c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0e2c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a0e2c-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a0e2c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a0e2c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0e2c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a0e2c-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a0e2c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0e2c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a0e2c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0e2c-125"><dt>Comctl32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a0e2c-125"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




