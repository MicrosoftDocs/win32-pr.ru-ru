---
title: Функции расширений NPS
description: Функции расширений NPS
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681678"
---
# <a name="nps-extensions-functions"></a><span data-ttu-id="1ff10-103">Функции расширений NPS</span><span class="sxs-lookup"><span data-stu-id="1ff10-103">NPS Extensions Functions</span></span>

> [!Note]  
> <span data-ttu-id="1ff10-104">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1ff10-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="1ff10-105">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="1ff10-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="1ff10-106">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="1ff10-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

## <a name="application-defined"></a><span data-ttu-id="1ff10-107">Определено приложением</span><span class="sxs-lookup"><span data-stu-id="1ff10-107">Application Defined</span></span>

<span data-ttu-id="1ff10-108">Архитектура библиотек DLL расширения NPS поддерживает следующие экспортированные функции:</span><span class="sxs-lookup"><span data-stu-id="1ff10-108">The architecture for NPS Extension DLLs supports the following exported functions:</span></span>

-   [<span data-ttu-id="1ff10-109">**радиусекстенсионфриаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="1ff10-109">**RadiusExtensionFreeAttributes**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [<span data-ttu-id="1ff10-110">**радиусекстенсионинит**</span><span class="sxs-lookup"><span data-stu-id="1ff10-110">**RadiusExtensionInit**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [<span data-ttu-id="1ff10-111">**радиусекстенсионпроцесс**</span><span class="sxs-lookup"><span data-stu-id="1ff10-111">**RadiusExtensionProcess**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [<span data-ttu-id="1ff10-112">**радиусекстенсионпроцессекс**</span><span class="sxs-lookup"><span data-stu-id="1ff10-112">**RadiusExtensionProcessEx**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [<span data-ttu-id="1ff10-113">**RadiusExtensionProcess2**</span><span class="sxs-lookup"><span data-stu-id="1ff10-113">**RadiusExtensionProcess2**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [<span data-ttu-id="1ff10-114">**радиусекстенсионтерм**</span><span class="sxs-lookup"><span data-stu-id="1ff10-114">**RadiusExtensionTerm**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

<span data-ttu-id="1ff10-115">Функции [**радиусекстенсионинит**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) и [**радиусекстенсионтерм**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="1ff10-115">The [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) and [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) functions are optional.</span></span>

<span data-ttu-id="1ff10-116">Библиотека DLL расширения может экспортировать [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) вместо [**радиусекстенсионпроцесс**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) или [**радиусекстенсионпроцессекс**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span><span class="sxs-lookup"><span data-stu-id="1ff10-116">The Extension DLL may export [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) instead of [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) or [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span></span>

<span data-ttu-id="1ff10-117">Если библиотека DLL расширения экспортирует [**радиусекстенсионпроцессекс**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), необходимо также экспортировать [**радиусекстенсионфриаттрибутес**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span><span class="sxs-lookup"><span data-stu-id="1ff10-117">If the Extension DLL exports [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), then it must also export [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span></span>

## <a name="system-defined"></a><span data-ttu-id="1ff10-118">Определено системой</span><span class="sxs-lookup"><span data-stu-id="1ff10-118">System Defined</span></span>

<span data-ttu-id="1ff10-119">Когда сервер политики сети вызывает реализацию [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS передает функции указатель на структуру [**\_ \_ управляющего \_ блока расширения RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .</span><span class="sxs-lookup"><span data-stu-id="1ff10-119">When NPS calls an implementation of [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS passes the function a pointer to a [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure.</span></span>

<span data-ttu-id="1ff10-120">[**\_ \_ Управляющая \_ Структура расширения RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) содержит указатели на функции для следующих функций, предоставляемых NPS:</span><span class="sxs-lookup"><span data-stu-id="1ff10-120">The [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="1ff10-121">[**Запрос на**](/previous-versions/ms688263(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ff10-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span></span>
-   <span data-ttu-id="1ff10-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ff10-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span></span>
-   <span data-ttu-id="1ff10-123">[**сетреспонсетипе**](/previous-versions/ms688462(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ff10-123">[**SetResponseType**](/previous-versions/ms688462(v=vs.85))</span></span>

<span data-ttu-id="1ff10-124">[**Функции GetResponse**](/previous-versions/ms688263(v=vs.85)) и [**GetResponse**](/previous-versions/ms688270(v=vs.85)) возвращают указатели на структуру типа [**\_ \_ массива атрибутов RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span><span class="sxs-lookup"><span data-stu-id="1ff10-124">The functions [**GetRequest**](/previous-versions/ms688263(v=vs.85)) and [**GetResponse**](/previous-versions/ms688270(v=vs.85)) return pointers to a structure of type [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span></span>

<span data-ttu-id="1ff10-125">Структура [**\_ \_ массива атрибутов RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) содержит указатели на функции для следующих функций, предоставляемых NPS:</span><span class="sxs-lookup"><span data-stu-id="1ff10-125">The [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="1ff10-126">[**Добавить**](/previous-versions/ms688246(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ff10-126">[**Add**](/previous-versions/ms688246(v=vs.85))</span></span>
-   <span data-ttu-id="1ff10-127">[**аттрибутеат**](/previous-versions/ms688253(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ff10-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span></span>
-   <span data-ttu-id="1ff10-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ff10-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span></span>
-   <span data-ttu-id="1ff10-129">[**инсертат**](/previous-versions/ms688296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ff10-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span></span>
-   <span data-ttu-id="1ff10-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ff10-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span></span>
-   <span data-ttu-id="1ff10-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ff10-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span></span>

 

 