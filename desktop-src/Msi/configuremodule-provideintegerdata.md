---
description: Метод Провидеинтежердата объекта Конфигуремодуле вызывается Mergemod.dll для получения целочисленных данных из клиентского средства.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Конфигуремодуле. Провидеинтежердата, метод (Мержемод. h)
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
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669279"
---
# <a name="configuremoduleprovideintegerdata-method"></a><span data-ttu-id="5105b-103">Конфигуремодуле. Провидеинтежердата, метод</span><span class="sxs-lookup"><span data-stu-id="5105b-103">ConfigureModule.ProvideIntegerData method</span></span>

<span data-ttu-id="5105b-104">Метод **провидеинтежердата** [**объекта конфигуремодуле**](configuremodule-object.md) вызывается Mergemod.dll для получения целочисленных данных из клиентского средства.</span><span class="sxs-lookup"><span data-stu-id="5105b-104">The **ProvideIntegerData** method of the [**ConfigureModule object**](configuremodule-object.md) is called by Mergemod.dll to retrieve integer data from the client tool.</span></span>

<span data-ttu-id="5105b-105">Mergemod.dll предоставляет *имя* из соответствующей записи в [таблице модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="5105b-105">Mergemod.dll provides the *Name* from the corresponding entry in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="5105b-106">Средство должно вернуть S \_ OK и предоставить соответствующее целое число настройки в *конфигдата*.</span><span class="sxs-lookup"><span data-stu-id="5105b-106">The tool should return S\_OK and provide the appropriate customization integer in *ConfigData*.</span></span>

<span data-ttu-id="5105b-107">Если средство не предоставляет данные конфигурации для этого значения *имени* , функция должна вернуть значение \_ false.</span><span class="sxs-lookup"><span data-stu-id="5105b-107">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="5105b-108">В этом случае Mergemod.dll игнорирует значение аргумента *конфигдата* и использует значение по умолчанию из таблицы модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="5105b-108">In this case Mergemod.dll ignores the value of the *ConfigData* argument and uses the Default value from the ModuleConfiguration table.</span></span>

## <a name="syntax"></a><span data-ttu-id="5105b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5105b-109">Syntax</span></span>


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="5105b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5105b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5105b-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="5105b-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="5105b-112">Имя элемента, для которого извлекаются данные.</span><span class="sxs-lookup"><span data-stu-id="5105b-112">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="5105b-113">*конфигдата*</span><span class="sxs-lookup"><span data-stu-id="5105b-113">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="5105b-114">Указатель на текст настройки.</span><span class="sxs-lookup"><span data-stu-id="5105b-114">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5105b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5105b-115">Return value</span></span>

<span data-ttu-id="5105b-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5105b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5105b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5105b-117">Remarks</span></span>

<span data-ttu-id="5105b-118">Клиент может быть вызван не более одного раза для каждой записи в [таблице модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="5105b-118">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="5105b-119">Обратите внимание, что Mergemod.dll никогда не выполняет несколько вызовов клиента для одного и того же значения "Name".</span><span class="sxs-lookup"><span data-stu-id="5105b-119">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="5105b-120">Если в таблице Модулесубститутион нет записей, использующих свойство, запись в таблице Модулеконфигуратион не вызывает клиент.</span><span class="sxs-lookup"><span data-stu-id="5105b-120">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="5105b-121">C++</span><span class="sxs-lookup"><span data-stu-id="5105b-121">C++</span></span>

<span data-ttu-id="5105b-122">См. раздел [**функция провидеинтежердата**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span><span class="sxs-lookup"><span data-stu-id="5105b-122">See [**ProvideIntegerData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="5105b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5105b-123">Requirements</span></span>



| <span data-ttu-id="5105b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5105b-124">Requirement</span></span> | <span data-ttu-id="5105b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5105b-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5105b-126">Версия</span><span class="sxs-lookup"><span data-stu-id="5105b-126">Version</span></span><br/> | <span data-ttu-id="5105b-127">Mergemod.dll 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5105b-127">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5105b-128">Header</span><span class="sxs-lookup"><span data-stu-id="5105b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5105b-129"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="5105b-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5105b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5105b-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="5105b-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5105b-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




