---
description: Метод Провидетекстдата вызывается Mergemod.dll для получения текстовых данных из клиентского средства. Mergemod.dll предоставляет имя из соответствующей записи в таблице Модулеконфигуратион.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: Конфигуремодуле. Провидетекстдата, метод (Мержемод. h)
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
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652193"
---
# <a name="configuremoduleprovidetextdata-method"></a><span data-ttu-id="a0afc-104">Конфигуремодуле. Провидетекстдата, метод</span><span class="sxs-lookup"><span data-stu-id="a0afc-104">ConfigureModule.ProvideTextData method</span></span>

<span data-ttu-id="a0afc-105">Метод **провидетекстдата** вызывается Mergemod.dll для получения текстовых данных из клиентского средства.</span><span class="sxs-lookup"><span data-stu-id="a0afc-105">The **ProvideTextData** method is called by Mergemod.dll to retrieve text data from the client tool.</span></span> <span data-ttu-id="a0afc-106">Mergemod.dll предоставляет *имя* из соответствующей записи в таблице модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="a0afc-106">Mergemod.dll provides the *Name* from the corresponding entry in the ModuleConfiguration table.</span></span>

<span data-ttu-id="a0afc-107">Средство должно вернуть S \_ OK и предоставить соответствующий текст настройки в конфигдата.</span><span class="sxs-lookup"><span data-stu-id="a0afc-107">The tool should return S\_OK and provide the appropriate customization text in ConfigData.</span></span> <span data-ttu-id="a0afc-108">Клиентское средство отвечает за выделение данных, но Mergemod.dllотвечает за освобождение памяти.</span><span class="sxs-lookup"><span data-stu-id="a0afc-108">The client tool is responsible for allocating the data, but Mergemod.dllis responsible for releasing the memory.</span></span> <span data-ttu-id="a0afc-109">Этот аргумент должен быть объектом **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="a0afc-109">This argument MUST be a **BSTR** object.</span></span> <span data-ttu-id="a0afc-110">**ЛПКВСТР** не принимается.</span><span class="sxs-lookup"><span data-stu-id="a0afc-110">**LPCWSTR** is NOT accepted.</span></span>

<span data-ttu-id="a0afc-111">Если средство не предоставляет данные конфигурации для этого значения *имени* , функция должна вернуть значение \_ false.</span><span class="sxs-lookup"><span data-stu-id="a0afc-111">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="a0afc-112">В этом случае Mergemod.dll игнорирует значение аргумента Конфигдата и использует значение по умолчанию из таблицы Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="a0afc-112">In this case Mergemod.dll ignores the value of the ConfigData argument and uses the Default value from the ModuleConfiguration table.</span></span>

<span data-ttu-id="a0afc-113">Любой код возврата, отличный от S \_ OK или \_ false, приведет к ошибке в журнале (если журнал открыт) и приведет к сбою слияния.</span><span class="sxs-lookup"><span data-stu-id="a0afc-113">Any return code other than S\_OK or S\_FALSE will cause an error to be logged (if a log is open) and will result in the merge failing.</span></span>

<span data-ttu-id="a0afc-114">Поскольку эта функция соответствует стандартному соглашению **BSTR** , значение NULL эквивалентно пустой строке.</span><span class="sxs-lookup"><span data-stu-id="a0afc-114">Because this function follows standard **BSTR** convention, null is equivalent to the empty string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0afc-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0afc-115">Syntax</span></span>


```JScript
ConfigureModule.ProvideTextData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="a0afc-116">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0afc-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0afc-117">*Name*</span><span class="sxs-lookup"><span data-stu-id="a0afc-117">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="a0afc-118">Имя элемента, для которого извлекаются данные.</span><span class="sxs-lookup"><span data-stu-id="a0afc-118">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="a0afc-119">*конфигдата*</span><span class="sxs-lookup"><span data-stu-id="a0afc-119">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="a0afc-120">Указатель на текст настройки.</span><span class="sxs-lookup"><span data-stu-id="a0afc-120">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0afc-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0afc-121">Return value</span></span>

<span data-ttu-id="a0afc-122">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a0afc-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0afc-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0afc-123">Remarks</span></span>

<span data-ttu-id="a0afc-124">Клиент может быть вызван не более одного раза для каждой записи в [таблице модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="a0afc-124">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="a0afc-125">Обратите внимание, что Mergemod.dll никогда не выполняет несколько вызовов клиента для одного и того же значения "Name".</span><span class="sxs-lookup"><span data-stu-id="a0afc-125">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="a0afc-126">Если в таблице Модулесубститутион нет записей, использующих свойство, запись в таблице Модулеконфигуратион не вызывает клиент.</span><span class="sxs-lookup"><span data-stu-id="a0afc-126">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="a0afc-127">C++</span><span class="sxs-lookup"><span data-stu-id="a0afc-127">C++</span></span>

<span data-ttu-id="a0afc-128">См. раздел [**функция провидетекстдата**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span><span class="sxs-lookup"><span data-stu-id="a0afc-128">See [**ProvideTextData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0afc-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a0afc-129">Requirements</span></span>



| <span data-ttu-id="a0afc-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a0afc-130">Requirement</span></span> | <span data-ttu-id="a0afc-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a0afc-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0afc-132">Версия</span><span class="sxs-lookup"><span data-stu-id="a0afc-132">Version</span></span><br/> | <span data-ttu-id="a0afc-133">Mergemod.dll 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a0afc-133">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="a0afc-134">Header</span><span class="sxs-lookup"><span data-stu-id="a0afc-134">Header</span></span><br/>  | <dl> <span data-ttu-id="a0afc-135"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0afc-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0afc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a0afc-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="a0afc-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0afc-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




