---
description: Перечисляет типы данных, используемые библиотеками DLL вложенной конфигурации безопасности и их вспомогательными функциями.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Типы данных управления безопасностью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663432"
---
# <a name="security-management-data-types"></a><span data-ttu-id="76749-103">Типы данных управления безопасностью</span><span class="sxs-lookup"><span data-stu-id="76749-103">Security Management Data Types</span></span>

<span data-ttu-id="76749-104">К типам данных управления безопасностью относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="76749-104">The security management data types include the following:</span></span>

-   [<span data-ttu-id="76749-105">Типы данных вложения</span><span class="sxs-lookup"><span data-stu-id="76749-105">Attachment Data Types</span></span>](#attachment-data-types)
-   [<span data-ttu-id="76749-106">Типы данных политики LSA</span><span class="sxs-lookup"><span data-stu-id="76749-106">LSA Policy Data Types</span></span>](#lsa-policy-data-types)

## <a name="attachment-data-types"></a><span data-ttu-id="76749-107">Типы данных вложения</span><span class="sxs-lookup"><span data-stu-id="76749-107">Attachment Data Types</span></span>

<span data-ttu-id="76749-108">Следующие типы данных используются библиотеками DLL вложенной конфигурации безопасности и их вспомогательными функциями.</span><span class="sxs-lookup"><span data-stu-id="76749-108">The following data types are used by the Security Configuration attachment DLLs and their supporting functions.</span></span>



| <span data-ttu-id="76749-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="76749-109">Data type</span></span>                                                    | <span data-ttu-id="76749-110">Описание</span><span class="sxs-lookup"><span data-stu-id="76749-110">Description</span></span>                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76749-111">**\_контекст ПЕРЕЧИСЛЕНИЯ \_ SCE**</span><span class="sxs-lookup"><span data-stu-id="76749-111">**SCE\_ENUMERATION\_CONTEXT**</span></span>](sce-enumeration-context.md) | <span data-ttu-id="76749-112">Используется функцией [**пфсце \_ запроса \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) для навигации по базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="76749-112">Used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>                                                                                                                                              |
| [<span data-ttu-id="76749-113">**\_обработчик SCE**</span><span class="sxs-lookup"><span data-stu-id="76749-113">**SCE\_HANDLE**</span></span>](sce-handle.md)                            | <span data-ttu-id="76749-114">Используется [**\_ \_ сведениями о запросе пфсце**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) и [**\_ \_ сведениями о задании пфсце**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) для передачи данных между вложением и базой данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="76749-114">Used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to pass information between the attachment and the security database.</span></span>                                                                                 |
| [<span data-ttu-id="76749-115">**сцестатус**</span><span class="sxs-lookup"><span data-stu-id="76749-115">**SCESTATUS**</span></span>](scestatus.md)                               | <span data-ttu-id="76749-116">Тип данных используется средством настройки безопасности API Set для получения сведений о результатах вызова функции.</span><span class="sxs-lookup"><span data-stu-id="76749-116">Data type is used by the Security Configuration tool set API to return information about the results of a function call.</span></span>                                                                                                                                    |
| [<span data-ttu-id="76749-117">**СЦЕСВК, \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="76749-117">**SCESVC\_HANDLE**</span></span>](scesvc-handle.md)                      | <span data-ttu-id="76749-118">Используется методами интерфейсов [**исцесвкаттачментдата**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) и [**исцесвкаттачментперсистинфо**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) для передачи данных между оснасткой настройки безопасности и расширением оснастки.</span><span class="sxs-lookup"><span data-stu-id="76749-118">Used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span> |
| [<span data-ttu-id="76749-119">**\_тип сведений \_ сцесвк**</span><span class="sxs-lookup"><span data-stu-id="76749-119">**SCESVC\_INFO\_TYPE**</span></span>](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | <span data-ttu-id="76749-120">Перечисление используется [**\_ \_ сведениями о запросе пфсце**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) и [**пфсце \_ Set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) для указания типа информации, запрашиваемой или передаваемой в базу данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="76749-120">Enumeration is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to indicate the type of information requested from or passed to the security database.</span></span>                                                 |



 

## <a name="lsa-policy-data-types"></a><span data-ttu-id="76749-121">Типы данных политики LSA</span><span class="sxs-lookup"><span data-stu-id="76749-121">LSA Policy Data Types</span></span>

<span data-ttu-id="76749-122">Функции управления политиками LSA используют следующие типы данных.</span><span class="sxs-lookup"><span data-stu-id="76749-122">The following data types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="76749-123">Тип данных</span><span class="sxs-lookup"><span data-stu-id="76749-123">Data type</span></span>                                                  | <span data-ttu-id="76749-124">Описание</span><span class="sxs-lookup"><span data-stu-id="76749-124">Description</span></span>                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="76749-125">**\_обработчик ПЕРЕЧИСЛЕНИЯ \_ LSA**</span><span class="sxs-lookup"><span data-stu-id="76749-125">**LSA\_ENUMERATION\_HANDLE**</span></span>](lsa-enumeration-handle.md) | <span data-ttu-id="76749-126">Используется для трассировки перечислений, в которых требуются несколько вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="76749-126">Used to track enumerations in which multiple function calls are required.</span></span> |
| [<span data-ttu-id="76749-127">**LSA \_ Handle**</span><span class="sxs-lookup"><span data-stu-id="76749-127">**LSA\_HANDLE**</span></span>](lsa-handle.md)                          | <span data-ttu-id="76749-128">Обработчик объекта [**политики**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="76749-128">Handle to a [**Policy**](policy-object.md) object.</span></span>                       |



 

 

 
