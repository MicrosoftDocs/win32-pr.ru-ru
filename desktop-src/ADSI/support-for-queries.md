---
title: Поддержка запросов
description: Реализуя интерфейс IDirectorySearch, поставщики ADSI получают доступ к подмножеству OLE DB функций только для чтения.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Поддержка запросов ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1304dcabd9c008b0f645982e695554225f59bac9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654099"
---
# <a name="support-for-queries"></a><span data-ttu-id="d9efe-104">Поддержка запросов</span><span class="sxs-lookup"><span data-stu-id="d9efe-104">Support for Queries</span></span>

<span data-ttu-id="d9efe-105">Реализуя интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , поставщики ADSI получают доступ к подмножеству OLE DB функций только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d9efe-105">By implementing the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, ADSI providers gain access to a subset of OLE DB read-only features.</span></span>

<span data-ttu-id="d9efe-106">Реализация ADSI методов [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) использует интерфейсы OLE DB, описанные в ADSI версии 1,0, включая следующий список COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="d9efe-106">The ADSI implementation of the methods of [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) itself uses the OLE DB interfaces described in ADSI Version 1.0, including the following list of COM objects:</span></span>

-   <span data-ttu-id="d9efe-107">Объект источника данных (Служба каталогов), поддерживающий **IDBInitialize**, **метода IDBCreateSession**, **интерфейс IDBProperties** и **IPersist**.</span><span class="sxs-lookup"><span data-stu-id="d9efe-107">Data Source Object (the directory service), supporting **IDBInitialize**, **IDBCreateSession**, **IDBProperties**, and **IPersist**.</span></span>
-   <span data-ttu-id="d9efe-108">Объект Дбсессионс, поддерживающий **IOpenRowSet**, **исессионпропертиес** и **икреатекомманд**.</span><span class="sxs-lookup"><span data-stu-id="d9efe-108">DBSessions Object, supporting **IOpenRowSet**, **ISessionProperties**, and **ICreateCommand**.</span></span>
-   <span data-ttu-id="d9efe-109">Объект Command, поддерживающий **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** и **Интерфейс IConvertType**.</span><span class="sxs-lookup"><span data-stu-id="d9efe-109">Command Object, supporting **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText**, and **IConvertType**.</span></span>
-   <span data-ttu-id="d9efe-110">Объект набора строк, поддерживающий **IAccessor**, **IColumnsInfo**, **Интерфейс IConvertType**, **IRowset** и **ировсетинфо**.</span><span class="sxs-lookup"><span data-stu-id="d9efe-110">Rowset Object, supporting **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset**, and **IRowsetInfo**.</span></span>

<span data-ttu-id="d9efe-111">Дополнительные сведения о OLE DB см. в разделе Справочник программиста по OLE DB в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="d9efe-111">For more information about OLE DB, see the OLE DB Programmer's Reference in the Platform Software Development Kit (SDK).</span></span>

 

 




