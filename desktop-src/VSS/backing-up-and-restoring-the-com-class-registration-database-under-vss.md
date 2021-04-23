---
description: Модель COM является двоичным стандартом для написания программного обеспечения компонентов в среде распределенных вычислений.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Резервное копирование и восстановление базы данных регистрации классов COM+ в VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae21489330693f0ce0d23b8639507121b9b00302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693702"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a><span data-ttu-id="5b929-103">Резервное копирование и восстановление базы данных регистрации классов COM+ в VSS</span><span class="sxs-lookup"><span data-stu-id="5b929-103">Backing Up and Restoring the COM+ Class Registration Database Under VSS</span></span>

<span data-ttu-id="5b929-104">Модель COM является двоичным стандартом для написания программного обеспечения компонентов в среде распределенных вычислений.</span><span class="sxs-lookup"><span data-stu-id="5b929-104">The Component Object Model (COM) is a binary standard for writing component software in a distributed computing environment.</span></span>

<span data-ttu-id="5b929-105">Исходная реализация Win32 идентификаторы компонентов (GUID) и другое состояние COM в реестре в **\_ \_ корневом \\ CLSID для классов hKey**.</span><span class="sxs-lookup"><span data-stu-id="5b929-105">The original Win32 implementation stored component identifiers (GUIDs) and other COM state in the registry under **HKEY\_CLASSES\_ROOT\\CLSID**.</span></span>

<span data-ttu-id="5b929-106">Текущее поколение объектной модели компонента COM+ предоставляет базу данных, не зависящую от реестра, для хранения сведений о регистрации компонента: база данных регистрации классов COM+.</span><span class="sxs-lookup"><span data-stu-id="5b929-106">The current generation of the Component Object Model, COM+, offers a registry-independent database for storing component registration information: the COM+ Class Registration Database.</span></span>

<span data-ttu-id="5b929-107">База данных регистрации классов COM+ поддерживает модуль записи VSS, который позволяет запрашивающим стороне создавать резервную копию базы данных регистрации с помощью данных, хранящихся на теневом томе.</span><span class="sxs-lookup"><span data-stu-id="5b929-107">The COM+ Class Registration Database supports a VSS writer, which allows requesters to back up the registration database using data stored on a shadow-copied volume.</span></span>

<span data-ttu-id="5b929-108">Чтобы восстановить базу данных регистрации COM+, инициатор запроса должен вызвать метод [икомадминкаталог:: ресторерегдб](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .</span><span class="sxs-lookup"><span data-stu-id="5b929-108">To restore the COM+ Registration Database, a requester must call the [ICOMAdminCatalog::RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="5b929-109">Дополнительные сведения о модуле записи базы данных регистрации COM+ см. [в разделе модули записи VSS в Box](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="5b929-109">For more information about the COM+ Registration Database writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
