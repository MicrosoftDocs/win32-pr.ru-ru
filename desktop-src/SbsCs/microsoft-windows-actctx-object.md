---
description: Объект Microsoft. Windows. Акткткс ссылается на манифесты и предоставляет обработчикам сценариев возможность доступа к параллельным сборкам. Объект Microsoft. Windows. Акткткс можно использовать для создания экземпляра параллельной сборки с COM-компонентами.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Объект Microsoft. Windows. Акткткс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908831"
---
# <a name="microsoftwindowsactctx-object"></a><span data-ttu-id="06b20-104">Объект Microsoft. Windows. Акткткс</span><span class="sxs-lookup"><span data-stu-id="06b20-104">Microsoft.Windows.ActCtx object</span></span>

<span data-ttu-id="06b20-105">Объект **Microsoft. Windows. акткткс** ссылается на манифесты и предоставляет обработчикам сценариев возможность доступа к параллельным сборкам.</span><span class="sxs-lookup"><span data-stu-id="06b20-105">The **Microsoft.Windows.ActCtx** object references manifests and provides a way for scripting engines to access side-by-side assemblies.</span></span> <span data-ttu-id="06b20-106">Объект **Microsoft. Windows. акткткс** можно использовать для создания экземпляра параллельной сборки с COM-компонентами.</span><span class="sxs-lookup"><span data-stu-id="06b20-106">The **Microsoft.Windows.ActCtx** object can be used to create an instance of a side-by-side assembly with COM components.</span></span>

<span data-ttu-id="06b20-107">Объект **Microsoft. Windows. акткткс** поставляется как сборка в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="06b20-107">The **Microsoft.Windows.ActCtx** object comes as an assembly in Windows Server 2003.</span></span> <span data-ttu-id="06b20-108">Она также может быть установлена приложениями, которые используют установщик Windows для установки и включают его в пакет установки в качестве модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="06b20-108">It can also be installed by applications that use the Windows Installer for setup and include it as a merge module in their installation package.</span></span>

## <a name="members"></a><span data-ttu-id="06b20-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="06b20-109">Members</span></span>

<span data-ttu-id="06b20-110">Объект **Microsoft. Windows. акткткс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="06b20-110">The **Microsoft.Windows.ActCtx** object has these types of members:</span></span>

-   [<span data-ttu-id="06b20-111">Методы</span><span class="sxs-lookup"><span data-stu-id="06b20-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="06b20-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="06b20-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="06b20-113">Методы</span><span class="sxs-lookup"><span data-stu-id="06b20-113">Methods</span></span>

<span data-ttu-id="06b20-114">Объект **Microsoft. Windows. акткткс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="06b20-114">The **Microsoft.Windows.ActCtx** object has these methods.</span></span>



| <span data-ttu-id="06b20-115">Метод</span><span class="sxs-lookup"><span data-stu-id="06b20-115">Method</span></span>                               | <span data-ttu-id="06b20-116">Описание</span><span class="sxs-lookup"><span data-stu-id="06b20-116">Description</span></span>                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="06b20-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="06b20-117">**CreateObject**</span></span>](createobject.md) | <span data-ttu-id="06b20-118">Создает объект в контексте текущего манифеста.</span><span class="sxs-lookup"><span data-stu-id="06b20-118">Creates an object in the context of the current manifest.</span></span><br/>            |
| [<span data-ttu-id="06b20-119">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="06b20-119">**GetObject**</span></span>](getobject.md)       | <span data-ttu-id="06b20-120">Возвращает экземпляр существующего объекта **Microsoft. Windows. акткткс** .</span><span class="sxs-lookup"><span data-stu-id="06b20-120">Gets an instance of an existing **Microsoft.Windows.ActCtx** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="06b20-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="06b20-121">Properties</span></span>

<span data-ttu-id="06b20-122">Объект **Microsoft. Windows. акткткс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="06b20-122">The **Microsoft.Windows.ActCtx** object has these properties.</span></span>



| <span data-ttu-id="06b20-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="06b20-123">Property</span></span>                                | <span data-ttu-id="06b20-124">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="06b20-124">Access type</span></span>          | <span data-ttu-id="06b20-125">Описание</span><span class="sxs-lookup"><span data-stu-id="06b20-125">Description</span></span>                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [<span data-ttu-id="06b20-126">**Явление**</span><span class="sxs-lookup"><span data-stu-id="06b20-126">**Manifest**</span></span>](manifest.md)<br/> | <span data-ttu-id="06b20-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="06b20-127">Read-only</span></span><br/> | <span data-ttu-id="06b20-128">Возвращает активный контекст активации.</span><span class="sxs-lookup"><span data-stu-id="06b20-128">Gets the active activation context.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="06b20-129">Требования</span><span class="sxs-lookup"><span data-stu-id="06b20-129">Requirements</span></span>



| <span data-ttu-id="06b20-130">Требование</span><span class="sxs-lookup"><span data-stu-id="06b20-130">Requirement</span></span> | <span data-ttu-id="06b20-131">Значение</span><span class="sxs-lookup"><span data-stu-id="06b20-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="06b20-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06b20-132">Minimum supported client</span></span><br/> | <span data-ttu-id="06b20-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="06b20-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="06b20-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06b20-134">Minimum supported server</span></span><br/> | <span data-ttu-id="06b20-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06b20-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




