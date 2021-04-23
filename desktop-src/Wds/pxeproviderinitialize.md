---
title: Функция обратного вызова Пксепровидеринитиализе
description: Экспорт из библиотеки динамической компоновки (DLL) поставщика, которая инициализирует поставщик и подготавливает его для получения запросов клиентов.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Функция обратного вызова Пксепровидеринитиализе службы развертывания Windows
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701091"
---
# <a name="pxeproviderinitialize-callback-function"></a><span data-ttu-id="d7287-104">Функция обратного вызова Пксепровидеринитиализе</span><span class="sxs-lookup"><span data-stu-id="d7287-104">PxeProviderInitialize callback function</span></span>

<span data-ttu-id="d7287-105">Экспорт из библиотеки динамической компоновки (DLL) поставщика, которая инициализирует поставщик и подготавливает его для получения запросов клиентов.</span><span class="sxs-lookup"><span data-stu-id="d7287-105">An export from a provider dynamic-link library (DLL) that initializes the provider and prepares it to receive client requests.</span></span> <span data-ttu-id="d7287-106">Для экспорта функции *пксепровидеринитиализе* требуются поставщики.</span><span class="sxs-lookup"><span data-stu-id="d7287-106">Providers are required to export the *PxeProviderInitialize* function.</span></span> <span data-ttu-id="d7287-107">Любые обратные вызовы поставщика должны быть зарегистрированы при вызове функции [**пксерегистеркаллбакк**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) во время обработки *пксепровидеринитиализе*.</span><span class="sxs-lookup"><span data-stu-id="d7287-107">Any callbacks to the provider must be registered with a call to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function during the processing of *PxeProviderInitialize*.</span></span> <span data-ttu-id="d7287-108">При возврате этой функции поставщик должен быть полностью инициализирован и готов к обработке клиентских запросов.</span><span class="sxs-lookup"><span data-stu-id="d7287-108">On the return of this function, the provider must be fully initialized and ready to process client requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7287-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7287-109">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a><span data-ttu-id="d7287-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7287-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7287-111">*хпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7287-111">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7287-112">Обработчик экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="d7287-112">Handle to the provider instance.</span></span> <span data-ttu-id="d7287-113">Этот обработчик должен храниться поставщиком и использоваться во всех последующих вызовах.</span><span class="sxs-lookup"><span data-stu-id="d7287-113">This handle must be stored by the provider and used in any subsequent calls.</span></span> <span data-ttu-id="d7287-114">Этот маркер действителен до вызова функции обратного вызова [*пксепровидершутдовн*](pxeprovidershutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="d7287-114">This handle is valid until the [*PxeProviderShutdown*](pxeprovidershutdown.md) callback function is called.</span></span>

</dd> <dt>

<span data-ttu-id="d7287-115">*хпровидеркэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7287-115">*hProviderKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7287-116">Обработчик раздела реестра, в котором хранятся сведения о конфигурации поставщика.</span><span class="sxs-lookup"><span data-stu-id="d7287-116">Handle to a registry key where provider configuration information is to be stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7287-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7287-117">Return value</span></span>

<span data-ttu-id="d7287-118">Если инициализация поставщика завершается успешно, обратный вызов должен возвращать **ошибку \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="d7287-118">If the provider initialization succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="d7287-119">В случае сбоя должен возвращаться соответствующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="d7287-119">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7287-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d7287-120">Requirements</span></span>



| <span data-ttu-id="d7287-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d7287-121">Requirement</span></span> | <span data-ttu-id="d7287-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d7287-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7287-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7287-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d7287-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d7287-124">None supported</span></span><br/>                                                          |
| <span data-ttu-id="d7287-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7287-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d7287-126">Windows Server 2008, Windows Server 2003 с пакетом обновления 2 (SP2), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7287-126">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7287-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7287-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7287-128">Функции сервера служб развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="d7287-128">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="d7287-129">*пксепровидершутдовн*</span><span class="sxs-lookup"><span data-stu-id="d7287-129">*PxeProviderShutdown*</span></span>](pxeprovidershutdown.md)
</dt> </dl>

 

 





