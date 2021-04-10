---
title: Коды ошибок (Уиаутоматионкореапи. h)
description: В этом разделе описываются коды ошибок, предоставляемые Microsoft UI Automation.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071048"
---
# <a name="error-codes-uiautomationcoreapih"></a><span data-ttu-id="98c83-103">Коды ошибок (Уиаутоматионкореапи. h)</span><span class="sxs-lookup"><span data-stu-id="98c83-103">Error Codes (UIAutomationCoreApi.h)</span></span>

<span data-ttu-id="98c83-104">В этом разделе описываются коды ошибок, предоставляемые Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="98c83-104">This topic describes the error codes exposed by Microsoft UI Automation.</span></span> <span data-ttu-id="98c83-105">Список сортируется в алфавитном порядке по имени.</span><span class="sxs-lookup"><span data-stu-id="98c83-105">The list is sorted alphabetically by name.</span></span>



| <span data-ttu-id="98c83-106">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="98c83-106">Constant/value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="98c83-107">Описание</span><span class="sxs-lookup"><span data-stu-id="98c83-107">Description</span></span>                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <span data-ttu-id="98c83-108"><dt>**UIA \_ E \_ елементнотаваилабле**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="98c83-108"><dt>**UIA\_E\_ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span></span> </dl>          | <span data-ttu-id="98c83-109">Указывает, что метод был вызван для виртуализированного элемента или для элемента, который больше не существует, обычно потому, что он был уничтожен.</span><span class="sxs-lookup"><span data-stu-id="98c83-109">Indicates that a method was called on a virtualized element, or on an element that no longer exists, usually because it has been destroyed.</span></span> <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <span data-ttu-id="98c83-110"><dt>**UIA \_ E \_ елементнотенаблед**</dt> <dt>0x80040200</dt></span><span class="sxs-lookup"><span data-stu-id="98c83-110"><dt>**UIA\_E\_ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span></span> </dl>                | <span data-ttu-id="98c83-111">Указывает, что метод, которому требуется включенный элемент, такой как [**SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) или [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), был вызван для элемента, который был отключен.</span><span class="sxs-lookup"><span data-stu-id="98c83-111">Indicates that a method that requires an enabled element, such as [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) or [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), was called on an element that was disabled.</span></span> <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <span data-ttu-id="98c83-112"><dt>**UIA \_ E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt></span><span class="sxs-lookup"><span data-stu-id="98c83-112"><dt>**UIA\_E\_INVALIDOPERATION**</dt> <dt>0x80131509</dt></span></span> </dl>                   | <span data-ttu-id="98c83-113">Указывает, что метод попытался выполнить операцию, которая является недопустимой.</span><span class="sxs-lookup"><span data-stu-id="98c83-113">Indicates that the method attempted an operation that was not valid.</span></span><br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <span data-ttu-id="98c83-114"><dt>**UIA \_ E \_ нокликкаблепоинт**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="98c83-114"><dt>**UIA\_E\_NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span></span> </dl>                   | <span data-ttu-id="98c83-115">Указывает, что метод [**жеткликкаблепоинт**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) был вызван для элемента, который не имеет точки, которую нельзя щелкнуть.</span><span class="sxs-lookup"><span data-stu-id="98c83-115">Indicates that the [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) method was called on an element that has no clickable point.</span></span><br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <span data-ttu-id="98c83-116"><dt>**UIA \_ E \_ NOTSUPPORTED**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="98c83-116"><dt>**UIA\_E\_NOTSUPPORTED**</dt> <dt>0x80040204</dt></span></span> </dl>                               | <span data-ttu-id="98c83-117">Указывает, что поставщик явно не поддерживает указанное свойство или шаблон элемента управления.</span><span class="sxs-lookup"><span data-stu-id="98c83-117">Indicates that the provider explicitly does not support the specified property or control pattern.</span></span> <span data-ttu-id="98c83-118">Модель автоматизации пользовательского интерфейса возвратит этот код ошибки вызывающему объекту без попытки предоставить значение по умолчанию или вернуться к другому поставщику.</span><span class="sxs-lookup"><span data-stu-id="98c83-118">UI Automation will return this error code to the caller without attempting to provide a default value or falling back to another provider.</span></span><br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <span data-ttu-id="98c83-119"><dt>**UIA \_ E \_ проксяссемблинотлоадед**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="98c83-119"><dt>**UIA\_E\_PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span></span> </dl> | <span data-ttu-id="98c83-120">Указывает, что возникла проблема при загрузке сборки, содержащей клиентский поставщик (прокси-сервер).</span><span class="sxs-lookup"><span data-stu-id="98c83-120">Indicates that a problem occurred when loading an assembly that contains a client-side (proxy) provider.</span></span><br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <span data-ttu-id="98c83-121"><dt>**UIA \_ E \_ timeout**</dt> <dt>0x80131505</dt></span><span class="sxs-lookup"><span data-stu-id="98c83-121"><dt>**UIA\_E\_TIMEOUT**</dt> <dt>0x80131505</dt></span></span> </dl>                                                      | <span data-ttu-id="98c83-122">Указывает, что время, выделенное для процесса или операции, истекло.</span><span class="sxs-lookup"><span data-stu-id="98c83-122">Indicates that the time allotted for a process or operation has expired.</span></span><br/>                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="98c83-123">Требования</span><span class="sxs-lookup"><span data-stu-id="98c83-123">Requirements</span></span>



| <span data-ttu-id="98c83-124">Требование</span><span class="sxs-lookup"><span data-stu-id="98c83-124">Requirement</span></span> | <span data-ttu-id="98c83-125">Значение</span><span class="sxs-lookup"><span data-stu-id="98c83-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98c83-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98c83-126">Minimum supported client</span></span><br/> | <span data-ttu-id="98c83-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="98c83-127">Windows XP \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="98c83-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98c83-128">Minimum supported server</span></span><br/> | <span data-ttu-id="98c83-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="98c83-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="98c83-130">Header</span><span class="sxs-lookup"><span data-stu-id="98c83-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="98c83-131"><dt>Уиаутоматионкореапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="98c83-131"><dt>UIAutomationCoreApi.h</dt></span></span> </dl> |



 

 





