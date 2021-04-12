---
description: Защита ресурсов предотвращает замену системных файлов и папок и разделов реестра, необходимых операционной системе. Изменение защищенных ресурсов может привести к сбою приложения или системы.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: защита ресурсов Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347215"
---
# <a name="windows-resource-protection"></a><span data-ttu-id="5c19b-104">защита ресурсов Windows</span><span class="sxs-lookup"><span data-stu-id="5c19b-104">Windows Resource Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="5c19b-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="5c19b-105">Purpose</span></span>

<span data-ttu-id="5c19b-106">Защита ресурсов Windows (WRP) предотвращает замену необходимых системных файлов, папок и разделов реестра, которые устанавливаются в составе операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5c19b-106">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="5c19b-107">Она стала доступной начиная с Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5c19b-107">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="5c19b-108">Приложения не должны перезаписывать эти ресурсы, так как они используются системой и другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="5c19b-108">Applications should not overwrite these resources because they are used by the system and other applications.</span></span> <span data-ttu-id="5c19b-109">Защита этих ресурсов предотвращает сбои приложений и операционных систем.</span><span class="sxs-lookup"><span data-stu-id="5c19b-109">Protecting these resources prevents application and operating system failures.</span></span> <span data-ttu-id="5c19b-110">WRP — это новое имя для защиты файлов Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="5c19b-110">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="5c19b-111">WRP защищает разделы и папки реестра, а также ключевые системные файлы.</span><span class="sxs-lookup"><span data-stu-id="5c19b-111">WRP protects registry keys and folders as well as essential system files.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5c19b-112">Где применимо</span><span class="sxs-lookup"><span data-stu-id="5c19b-112">Where applicable</span></span>

<span data-ttu-id="5c19b-113">Все приложения на базе Windows и программы установки, работающие под управлением Windows Server 2008 или Windows Vista и более поздних операционных систем, должны учитывать WRP.</span><span class="sxs-lookup"><span data-stu-id="5c19b-113">All Windows-based applications and their installation programs that run on Windows Server 2008 or Windows Vista, and later operating systems, should be aware of WRP.</span></span> <span data-ttu-id="5c19b-114">Все приложения на базе Windows, работающие на Microsoft Windows Server 2003 или Windows XP, и программы установки должны знать о WFP.</span><span class="sxs-lookup"><span data-stu-id="5c19b-114">All Windows-based applications that run on Microsoft Windows Server 2003 or Windows XP and their installation programs should be aware of WFP.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5c19b-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="5c19b-115">Developer audience</span></span>

<span data-ttu-id="5c19b-116">API WRP предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="5c19b-116">The WRP API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="5c19b-117">API WRP имеет две функции: [**сфЦисфилепротектед**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) и [**сфЦискэйпротектед**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span><span class="sxs-lookup"><span data-stu-id="5c19b-117">The WRP API has two functions: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5c19b-118">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="5c19b-118">Run-time requirements</span></span>

<span data-ttu-id="5c19b-119">Для приложений, использующих только функцию [**сфЦисфилепротектед**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) , требуется windows Server 2008, Windows Vista, windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5c19b-119">Applications that use only the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) function require Windows Server 2008, Windows Vista, Windows Server 2003, or Windows XP.</span></span> <span data-ttu-id="5c19b-120">Для приложений, использующих функцию [**сфЦискэйпротектед**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) , требуется windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5c19b-120">Applications that use the [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) function require Windows Server 2008 or Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5c19b-121">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="5c19b-121">In this section</span></span>



| <span data-ttu-id="5c19b-122">Раздел</span><span class="sxs-lookup"><span data-stu-id="5c19b-122">Topic</span></span>                                                                                     | <span data-ttu-id="5c19b-123">Описание</span><span class="sxs-lookup"><span data-stu-id="5c19b-123">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="5c19b-124">О защита ресурсов Windows</span><span class="sxs-lookup"><span data-stu-id="5c19b-124">About Windows Resource Protection</span></span>](about-windows-file-protection.md)<br/>         | <span data-ttu-id="5c19b-125">Общие сведения о WRP.</span><span class="sxs-lookup"><span data-stu-id="5c19b-125">General information about WRP.</span></span><br/>   |
| [<span data-ttu-id="5c19b-126">Справочник по защита ресурсов Windows</span><span class="sxs-lookup"><span data-stu-id="5c19b-126">Windows Resource Protection Reference</span></span>](windows-file-protection-reference.md)<br/> | <span data-ttu-id="5c19b-127">Справочная документация по WRP.</span><span class="sxs-lookup"><span data-stu-id="5c19b-127">Reference documentation for WRP.</span></span><br/> |



 

 

 




