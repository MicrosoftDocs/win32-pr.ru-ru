---
title: Метод инициализации Ирдвтаскплугин
description: Вызывается для инициализации агента задачи.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Инициализация метода службы удаленных рабочих столов
- Инициализация метода службы удаленных рабочих столов, интерфейс Ирдвтаскплугин
- Интерфейс Ирдвтаскплугин службы удаленных рабочих столов, метод Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415032"
---
# <a name="irdvtaskplugininitialize-method"></a><span data-ttu-id="7cee9-106">Метод Ирдвтаскплугин:: Initialize</span><span class="sxs-lookup"><span data-stu-id="7cee9-106">IRDVTaskPlugin::Initialize method</span></span>

<span data-ttu-id="7cee9-107">Вызывается для инициализации агента задачи.</span><span class="sxs-lookup"><span data-stu-id="7cee9-107">Called to initialize the task agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cee9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cee9-108">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a><span data-ttu-id="7cee9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cee9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cee9-110">*пнотифисинк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cee9-110">*pNotifySink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cee9-111">Тип: \**[**ирдвтаскплугиннотифисинк**](irdvtaskpluginnotifysink.md) \** _</span><span class="sxs-lookup"><span data-stu-id="7cee9-111">Type: \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\** _</span></span>

<span data-ttu-id="7cee9-112">Указатель на интерфейс [_ *ирдвтаскплугиннотифисинк* \*](irdvtaskpluginnotifysink.md) , который агент задачи использует для взаимодействия с агентом триггера.</span><span class="sxs-lookup"><span data-stu-id="7cee9-112">A pointer to an [_ *IRDVTaskPluginNotifySink*\*](irdvtaskpluginnotifysink.md) interface that the task agent uses to communicate with the trigger agent.</span></span> <span data-ttu-id="7cee9-113">Этот интерфейс необходимо освобождать, если он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="7cee9-113">You must release this interface when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cee9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cee9-114">Return value</span></span>

<span data-ttu-id="7cee9-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7cee9-115">Type: **HRESULT**</span></span>

<span data-ttu-id="7cee9-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7cee9-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7cee9-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7cee9-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cee9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7cee9-118">Requirements</span></span>



| <span data-ttu-id="7cee9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7cee9-119">Requirement</span></span> | <span data-ttu-id="7cee9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7cee9-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="7cee9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7cee9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7cee9-122">Windows 7 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="7cee9-122">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="7cee9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7cee9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7cee9-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7cee9-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7cee9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cee9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cee9-126">**ирдвтаскплугин**</span><span class="sxs-lookup"><span data-stu-id="7cee9-126">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





