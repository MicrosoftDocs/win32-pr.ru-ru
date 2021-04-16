---
title: Класс Win32_RDMSEnvironment
description: Управляет средой служб управления удаленный рабочий стол (RDMS).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSEnvironment службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSEnvironment, описание
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672616"
---
# <a name="win32_rdmsenvironment-class"></a><span data-ttu-id="265af-105">\_Класс Win32 рдмсенвиронмент</span><span class="sxs-lookup"><span data-stu-id="265af-105">Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="265af-106">Управляет средой служб управления удаленный рабочий стол (RDMS).</span><span class="sxs-lookup"><span data-stu-id="265af-106">Manages a Remote Desktop Management Services (RDMS) environment.</span></span>

<span data-ttu-id="265af-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="265af-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="265af-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="265af-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a><span data-ttu-id="265af-109">Члены</span><span class="sxs-lookup"><span data-stu-id="265af-109">Members</span></span>

<span data-ttu-id="265af-110">Класс **Win32 \_ рдмсенвиронмент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="265af-110">The **Win32\_RDMSEnvironment** class has these types of members:</span></span>

-   [<span data-ttu-id="265af-111">Методы</span><span class="sxs-lookup"><span data-stu-id="265af-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="265af-112">Методы</span><span class="sxs-lookup"><span data-stu-id="265af-112">Methods</span></span>

<span data-ttu-id="265af-113">Класс **Win32 \_ рдмсенвиронмент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="265af-113">The **Win32\_RDMSEnvironment** class has these methods.</span></span>



| <span data-ttu-id="265af-114">Метод</span><span class="sxs-lookup"><span data-stu-id="265af-114">Method</span></span>                                                                   | <span data-ttu-id="265af-115">Описание</span><span class="sxs-lookup"><span data-stu-id="265af-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="265af-116">**жетактивесервер**</span><span class="sxs-lookup"><span data-stu-id="265af-116">**GetActiveServer**</span></span>](getactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="265af-117">Возвращает полное доменное имя среды RDMS.</span><span class="sxs-lookup"><span data-stu-id="265af-117">Retrieves the fully qualified domain name (FQDN) of the RDMS environment.</span></span><br/>                 |
| [<span data-ttu-id="265af-118">**жетклиентакцесснаме**</span><span class="sxs-lookup"><span data-stu-id="265af-118">**GetClientAccessName**</span></span>](getclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="265af-119">Извлекает имя записи ресурса системы доменных имен (DNS) для среды RDMS.</span><span class="sxs-lookup"><span data-stu-id="265af-119">Retrieves the Domain Name System (DNS) resource record (RR) name of the RDMS environment.</span></span><br/> |
| [<span data-ttu-id="265af-120">**сетактивесервер**</span><span class="sxs-lookup"><span data-stu-id="265af-120">**SetActiveServer**</span></span>](setactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="265af-121">Задает полное доменное имя среды RDMS для текущего узла.</span><span class="sxs-lookup"><span data-stu-id="265af-121">Sets the FQDN of the RDMS environment to the current node.</span></span><br/>                                |
| [<span data-ttu-id="265af-122">**сетклиентакцесснаме**</span><span class="sxs-lookup"><span data-stu-id="265af-122">**SetClientAccessName**</span></span>](setclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="265af-123">Обновляет имя RR DNS среды RDMS.</span><span class="sxs-lookup"><span data-stu-id="265af-123">Updates the DNS RR name of the RDMS environment.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="265af-124">Требования</span><span class="sxs-lookup"><span data-stu-id="265af-124">Requirements</span></span>



| <span data-ttu-id="265af-125">Требование</span><span class="sxs-lookup"><span data-stu-id="265af-125">Requirement</span></span> | <span data-ttu-id="265af-126">Значение</span><span class="sxs-lookup"><span data-stu-id="265af-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="265af-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="265af-127">Minimum supported client</span></span><br/> | <span data-ttu-id="265af-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="265af-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="265af-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="265af-129">Minimum supported server</span></span><br/> | <span data-ttu-id="265af-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="265af-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="265af-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="265af-131">Namespace</span></span><br/>                | <span data-ttu-id="265af-132">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="265af-132">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="265af-133">MOF</span><span class="sxs-lookup"><span data-stu-id="265af-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="265af-134"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="265af-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="265af-135">DLL</span><span class="sxs-lookup"><span data-stu-id="265af-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="265af-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="265af-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="265af-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="265af-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="265af-138">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="265af-138">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





