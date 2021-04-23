---
title: Функция Вмдрмшутдовн (Вмдрмсдк. h)
description: Функция Вмдрмшутдовн освобождает ресурсы, используемые расширенными API-интерфейсами клиента DRM Windows Media.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- Вмдрмшутдовн функция Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674891"
---
# <a name="wmdrmshutdown-function"></a><span data-ttu-id="c0124-104">Функция Вмдрмшутдовн</span><span class="sxs-lookup"><span data-stu-id="c0124-104">WMDRMShutdown function</span></span>

<span data-ttu-id="c0124-105">Функция **вмдрмшутдовн** освобождает ресурсы, используемые расширенными API-интерфейсами клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c0124-105">The **WMDRMShutdown** function releases resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0124-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0124-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a><span data-ttu-id="c0124-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0124-107">Parameters</span></span>

<span data-ttu-id="c0124-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="c0124-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0124-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0124-109">Return value</span></span>

<span data-ttu-id="c0124-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c0124-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c0124-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c0124-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c0124-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c0124-112">Return code</span></span>                                                                          | <span data-ttu-id="c0124-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c0124-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c0124-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c0124-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c0124-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c0124-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0124-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0124-116">Remarks</span></span>

<span data-ttu-id="c0124-117">Чтобы избежать утечек памяти, необходимо вызвать эту функцию для каждого вызова функции [**вмдрмстартуп**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="c0124-117">To avoid memory leaks, you must call this function for every call of the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0124-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c0124-118">Requirements</span></span>



| <span data-ttu-id="c0124-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c0124-119">Requirement</span></span> | <span data-ttu-id="c0124-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c0124-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0124-121">Header</span><span class="sxs-lookup"><span data-stu-id="c0124-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c0124-122"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0124-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0124-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0124-123">Library</span></span><br/> | <dl> <span data-ttu-id="c0124-124"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0124-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="c0124-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c0124-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="c0124-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0124-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0124-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0124-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0124-128">**Функции**</span><span class="sxs-lookup"><span data-stu-id="c0124-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 





