---
title: Функция Вмдрмстартуп (Вмдрмсдк. h)
description: Функция Вмдрмстартуп инициализирует ресурсы, используемые расширенными API-интерфейсами клиента DRM Windows Media.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- Вмдрмстартуп функция Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c152a5160750f3c1943b455a8877b4615781b6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648900"
---
# <a name="wmdrmstartup-function"></a><span data-ttu-id="77218-104">Функция Вмдрмстартуп</span><span class="sxs-lookup"><span data-stu-id="77218-104">WMDRMStartup function</span></span>

<span data-ttu-id="77218-105">Функция **вмдрмстартуп** инициализирует ресурсы, используемые расширенными API-интерфейсами клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="77218-105">The **WMDRMStartup** function initializes resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="77218-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77218-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a><span data-ttu-id="77218-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="77218-107">Parameters</span></span>

<span data-ttu-id="77218-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="77218-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="77218-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77218-109">Return value</span></span>

<span data-ttu-id="77218-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="77218-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="77218-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="77218-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="77218-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="77218-112">Return code</span></span>                                                                          | <span data-ttu-id="77218-113">Описание</span><span class="sxs-lookup"><span data-stu-id="77218-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="77218-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="77218-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="77218-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="77218-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="77218-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77218-116">Remarks</span></span>

<span data-ttu-id="77218-117">Для каждого вызова этой функции необходимо вызвать [**вмдрмшутдовн**](wmdrmshutdown.md) , чтобы освободить используемые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="77218-117">For every call of this function, you must call [**WMDRMShutdown**](wmdrmshutdown.md) to release the resources used.</span></span>

## <a name="requirements"></a><span data-ttu-id="77218-118">Требования</span><span class="sxs-lookup"><span data-stu-id="77218-118">Requirements</span></span>



| <span data-ttu-id="77218-119">Требование</span><span class="sxs-lookup"><span data-stu-id="77218-119">Requirement</span></span> | <span data-ttu-id="77218-120">Значение</span><span class="sxs-lookup"><span data-stu-id="77218-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77218-121">Header</span><span class="sxs-lookup"><span data-stu-id="77218-121">Header</span></span><br/>  | <dl> <span data-ttu-id="77218-122"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="77218-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="77218-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="77218-123">Library</span></span><br/> | <dl> <span data-ttu-id="77218-124"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77218-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="77218-125">DLL</span><span class="sxs-lookup"><span data-stu-id="77218-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="77218-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77218-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77218-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77218-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77218-128">**Функции**</span><span class="sxs-lookup"><span data-stu-id="77218-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 





