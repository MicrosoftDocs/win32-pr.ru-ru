---
title: Функция Клеанупкредентиалкаче
description: Реализуется определенными поставщиками поддержки безопасности (SSP) для очистки кэша учетных данных поставщика общих служб.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- Функция Клеанупкредентиалкаче WinINet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135162"
---
# <a name="cleanupcredentialcache-function"></a><span data-ttu-id="51fde-104">Функция Клеанупкредентиалкаче</span><span class="sxs-lookup"><span data-stu-id="51fde-104">CleanupCredentialCache function</span></span>

<span data-ttu-id="51fde-105">Функция **клеанупкредентиалкаче** реализуется определенными поставщиками поддержки безопасности (SSP) для записи кэша учетных данных поставщика общих служб.</span><span class="sxs-lookup"><span data-stu-id="51fde-105">The **CleanupCredentialCache** function is implemented by certain Security Support Providers (SSP) to flush the SSP credential cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="51fde-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51fde-106">Syntax</span></span>


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a><span data-ttu-id="51fde-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="51fde-107">Parameters</span></span>

<span data-ttu-id="51fde-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="51fde-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51fde-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51fde-109">Return value</span></span>

<span data-ttu-id="51fde-110">**Значение true** , если функция выполнена. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="51fde-110">**TRUE** if the function succeeds; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="51fde-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51fde-111">Remarks</span></span>

<span data-ttu-id="51fde-112">Функция **клеанупкредентиалкаче** реализуется следующими поставщиками общих служб:</span><span class="sxs-lookup"><span data-stu-id="51fde-112">The **CleanupCredentialCache** function is implemented by the following SSPs:</span></span>

-   <span data-ttu-id="51fde-113">MSNSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="51fde-113">MSNSSPC.dll</span></span>
-   <span data-ttu-id="51fde-114">MSAPSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="51fde-114">MSAPSSPC.dll</span></span>

<span data-ttu-id="51fde-115">Реализация **клеанупкредентиалкаче** с помощью этих SSP всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="51fde-115">The implementation of **CleanupCredentialCache** by these SSPs always returns **TRUE**.</span></span>

<span data-ttu-id="51fde-116">Прежде чем пытаться получить маркер модуля для экспорта **клеанупкредентиалкаче**, приложение должно убедиться, что загруженный поставщик общих служб является одним из известных SSP, реализующих функцию **клеанупкредентиалкаче** .</span><span class="sxs-lookup"><span data-stu-id="51fde-116">Before attempting to obtain a module handle to export **CleanupCredentialCache**, the application must verify that the SSP that has been loaded is one of the known SSPs implementing the **CleanupCredentialCache** function.</span></span>

<span data-ttu-id="51fde-117">Чтобы очистить кэш учетных данных поставщика общих служб, приложение должно получить маркер модуля для поставщика общих служб, вызвав функцию [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="51fde-117">In order to flush the SSP credential cache, the application must obtain a module handle for the SSP by calling the [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span> <span data-ttu-id="51fde-118">После получения модуля приложение должно экспортировать функцию **клеанупкредентиалкаче** , реализованную поставщиком общих служб, вызвав функцию [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) , передав модуль, возвращенный **Ошибка GetModuleHandle** и **клеанупкредентиалкаче** , в качестве входных параметров.</span><span class="sxs-lookup"><span data-stu-id="51fde-118">After obtaining the module, the application should export the **CleanupCredentialCache** function implemented by the SSP by calling the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function, passing the module returned by **GetModuleHandle** and **CleanupCredentialCache** as input parameters.</span></span>

<span data-ttu-id="51fde-119">Как и все остальные аспекты API WinINet, эта функция не может быть безопасно вызвана из DllMain или конструкторов и деструкторов глобальных объектов.</span><span class="sxs-lookup"><span data-stu-id="51fde-119">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="51fde-120">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="51fde-120">WinINet does not support server implementations.</span></span> <span data-ttu-id="51fde-121">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="51fde-121">In addition, it should not be used from a service.</span></span> <span data-ttu-id="51fde-122">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="51fde-122">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51fde-123">Требования</span><span class="sxs-lookup"><span data-stu-id="51fde-123">Requirements</span></span>



| <span data-ttu-id="51fde-124">Требование</span><span class="sxs-lookup"><span data-stu-id="51fde-124">Requirement</span></span> | <span data-ttu-id="51fde-125">Значение</span><span class="sxs-lookup"><span data-stu-id="51fde-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fde-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51fde-126">Minimum supported client</span></span><br/> | <span data-ttu-id="51fde-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51fde-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="51fde-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51fde-128">Minimum supported server</span></span><br/> | <span data-ttu-id="51fde-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51fde-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                       |
| <span data-ttu-id="51fde-130">DLL</span><span class="sxs-lookup"><span data-stu-id="51fde-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51fde-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51fde-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span></span> </dl> |



 

