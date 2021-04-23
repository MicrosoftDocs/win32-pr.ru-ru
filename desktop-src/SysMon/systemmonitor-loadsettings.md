---
title: Системмонитор. Лоадсеттингс, метод
description: Добавляет счетчики из HTML-файла шаблона в системный монитор.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Метод Лоадсеттингс Сисмон
- Метод Лоадсеттингс Сисмон, объект Системмонитор
- Сисмон объекта Системмонитор, метод Лоадсеттингс
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415584"
---
# <a name="systemmonitorloadsettings-method"></a><span data-ttu-id="f47ef-106">Системмонитор. Лоадсеттингс, метод</span><span class="sxs-lookup"><span data-stu-id="f47ef-106">SystemMonitor.LoadSettings method</span></span>

<span data-ttu-id="f47ef-107">Добавляет счетчики из HTML-файла шаблона в системный монитор.</span><span class="sxs-lookup"><span data-stu-id="f47ef-107">Adds the counters in the HTML template file to the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="f47ef-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f47ef-108">Syntax</span></span>


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a><span data-ttu-id="f47ef-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f47ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f47ef-110">*Сеттингсфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f47ef-110">*SettingsFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f47ef-111">Строка HTML, указывающая счетчики, которые необходимо добавить в системный монитор.</span><span class="sxs-lookup"><span data-stu-id="f47ef-111">HTML string that specifies the counters to add to the System Monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f47ef-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f47ef-112">Return value</span></span>

<span data-ttu-id="f47ef-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f47ef-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f47ef-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f47ef-114">Remarks</span></span>

<span data-ttu-id="f47ef-115">Чтобы сохранить текущие счетчики в системном мониторе в HTML-файл, вызовите метод [**системмонитор. SaveAs**](systemmonitor-saveas.md) .</span><span class="sxs-lookup"><span data-stu-id="f47ef-115">To save the current counters in the System Monitor to an HTML file, call the [**SystemMonitor.SaveAs**](systemmonitor-saveas.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f47ef-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f47ef-116">Requirements</span></span>



| <span data-ttu-id="f47ef-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f47ef-117">Requirement</span></span> | <span data-ttu-id="f47ef-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f47ef-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f47ef-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f47ef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f47ef-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f47ef-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f47ef-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f47ef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f47ef-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f47ef-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f47ef-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f47ef-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f47ef-124"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f47ef-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f47ef-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f47ef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f47ef-126">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="f47ef-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





