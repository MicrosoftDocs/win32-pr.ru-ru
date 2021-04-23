---
description: Объект Конфигуремодуле — это интерфейс, реализуемый клиентом.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Объект Конфигуремодуле (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652195"
---
# <a name="configuremodule-object"></a><span data-ttu-id="220fd-103">Объект Конфигуремодуле</span><span class="sxs-lookup"><span data-stu-id="220fd-103">ConfigureModule object</span></span>

<span data-ttu-id="220fd-104">**Объект конфигуремодуле** — это интерфейс, реализуемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="220fd-104">The **ConfigureModule object** is an interface implemented by the client.</span></span> <span data-ttu-id="220fd-105">Mergemod.dllвызывает методы в интерфейсе **имсмконфигуремодуле** , чтобы запросить предоставление сведений о конфигурации клиентским средством.</span><span class="sxs-lookup"><span data-stu-id="220fd-105">Mergemod.dllcalls methods on the **IMsmConfigureModule** interface to request that the client tool provide configuration information.</span></span> <span data-ttu-id="220fd-106">Модуль настраивается на основе ответов клиента на вызовы этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="220fd-106">The module is configured based on the client's responses to calls on this interface.</span></span>

## <a name="members"></a><span data-ttu-id="220fd-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="220fd-107">Members</span></span>

<span data-ttu-id="220fd-108">Объект **конфигуремодуле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="220fd-108">The **ConfigureModule** object has these types of members:</span></span>

-   [<span data-ttu-id="220fd-109">Методы</span><span class="sxs-lookup"><span data-stu-id="220fd-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="220fd-110">Методы</span><span class="sxs-lookup"><span data-stu-id="220fd-110">Methods</span></span>

<span data-ttu-id="220fd-111">Объект **конфигуремодуле** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="220fd-111">The **ConfigureModule** object has these methods.</span></span>



| <span data-ttu-id="220fd-112">Метод</span><span class="sxs-lookup"><span data-stu-id="220fd-112">Method</span></span>                                                           | <span data-ttu-id="220fd-113">Описание</span><span class="sxs-lookup"><span data-stu-id="220fd-113">Description</span></span>                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="220fd-114">**провидеинтежердата**</span><span class="sxs-lookup"><span data-stu-id="220fd-114">**ProvideIntegerData**</span></span>](configuremodule-provideintegerdata.md) | <span data-ttu-id="220fd-115">Вызывается методом Mergemod.dll для получения целых чисел, используемых для настройки модуля.</span><span class="sxs-lookup"><span data-stu-id="220fd-115">Called by Mergemod.dll to obtain integers used to configure the module.</span></span><br/> |
| [<span data-ttu-id="220fd-116">**провидетекстдата**</span><span class="sxs-lookup"><span data-stu-id="220fd-116">**ProvideTextData**</span></span>](configuremodule-providetextdata.md)       | <span data-ttu-id="220fd-117">Вызывается Mergemod.dll для получения текста, используемого для настройки модуля.</span><span class="sxs-lookup"><span data-stu-id="220fd-117">Called by Mergemod.dll to obtain text used to configure the module.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="220fd-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="220fd-118">Remarks</span></span>

### <a name="c"></a><span data-ttu-id="220fd-119">C++</span><span class="sxs-lookup"><span data-stu-id="220fd-119">C++</span></span>

<span data-ttu-id="220fd-120">интерфейс **имсмконфигуремодуле: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="220fd-120">interface **IMsmConfigureModule : IDispatch**</span></span>

### <a name="interface-id"></a><span data-ttu-id="220fd-121">Идентификатор интерфейса</span><span class="sxs-lookup"><span data-stu-id="220fd-121">Interface ID</span></span>



| <span data-ttu-id="220fd-122">Константа</span><span class="sxs-lookup"><span data-stu-id="220fd-122">Constant</span></span>                     | <span data-ttu-id="220fd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="220fd-123">Value</span></span>                                  |
|------------------------------|----------------------------------------|
| <span data-ttu-id="220fd-124">**IID \_ имсмконфигуремодуле**</span><span class="sxs-lookup"><span data-stu-id="220fd-124">**IID\_IMsmConfigureModule**</span></span> | <span data-ttu-id="220fd-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span><span class="sxs-lookup"><span data-stu-id="220fd-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="220fd-126">Требования</span><span class="sxs-lookup"><span data-stu-id="220fd-126">Requirements</span></span>



| <span data-ttu-id="220fd-127">Требование</span><span class="sxs-lookup"><span data-stu-id="220fd-127">Requirement</span></span> | <span data-ttu-id="220fd-128">Значение</span><span class="sxs-lookup"><span data-stu-id="220fd-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="220fd-129">Версия</span><span class="sxs-lookup"><span data-stu-id="220fd-129">Version</span></span><br/> | <span data-ttu-id="220fd-130">Mergemod.dll 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="220fd-130">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="220fd-131">Header</span><span class="sxs-lookup"><span data-stu-id="220fd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="220fd-132"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="220fd-132"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="220fd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="220fd-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="220fd-134"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="220fd-134"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




