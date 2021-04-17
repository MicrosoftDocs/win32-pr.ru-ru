---
description: 'Запросы данных — это инструкции WQL, которые запрашивают экземпляры классов. Чтобы выдать запрос данных, приложения вызывают метод IWbemServices:: ExecQuery или IWbemServices:: Ексеккуерясинк.'
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Запрос данных экземпляра класса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32df053ae1267f396978d98271f57f174ea6bf0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693639"
---
# <a name="requesting-class-instance-data"></a><span data-ttu-id="60d89-104">Запрос данных экземпляра класса</span><span class="sxs-lookup"><span data-stu-id="60d89-104">Requesting Class Instance Data</span></span>

<span data-ttu-id="60d89-105">Запросы данных — это инструкции WQL, которые запрашивают экземпляры классов.</span><span class="sxs-lookup"><span data-stu-id="60d89-105">Data queries are WQL statements that request instances of classes.</span></span> <span data-ttu-id="60d89-106">Чтобы выдать запрос данных, приложения вызывают метод [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) или [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="60d89-106">To issue a data query, applications call the [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) or [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method.</span></span>

<span data-ttu-id="60d89-107">Для выполнения запросов данных используются следующие инструкции:</span><span class="sxs-lookup"><span data-stu-id="60d89-107">The following statements are used to make data queries:</span></span>

-   [<span data-ttu-id="60d89-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="60d89-108">SELECT</span></span>](select-statement-for-data-queries.md)
-   [<span data-ttu-id="60d89-109">СОЕДИНИТЕЛи</span><span class="sxs-lookup"><span data-stu-id="60d89-109">ASSOCIATORS OF</span></span>](associators-of-statement.md)
-   [<span data-ttu-id="60d89-110">ССЫЛКИ НА</span><span class="sxs-lookup"><span data-stu-id="60d89-110">REFERENCES OF</span></span>](references-of-statement.md)
-   [<span data-ttu-id="60d89-111">ISA</span><span class="sxs-lookup"><span data-stu-id="60d89-111">ISA</span></span>](isa-operator-for-data-queries.md)

<span data-ttu-id="60d89-112">Инструкция WQL SELECT — это стандартный оператор язык SQL (SQL) для получения сведений с помощью нескольких ограничений и расширений, характерных для WQL.</span><span class="sxs-lookup"><span data-stu-id="60d89-112">The WQL SELECT statement is the standard Structured Query Language (SQL) statement for retrieving information, with a few restrictions and extensions specific to WQL.</span></span> <span data-ttu-id="60d89-113">Хотя инструкция SQL SELECT обычно используется в среде базы данных для извлечения определенных столбцов из таблиц, в WMI используется инструкция WQL SELECT для получения экземпляров одного класса.</span><span class="sxs-lookup"><span data-stu-id="60d89-113">Although the SQL SELECT statement is typically used in the database environment to retrieve particular columns from tables, the WQL SELECT statement is used in WMI to retrieve instances of a single class.</span></span> <span data-ttu-id="60d89-114">WQL не поддерживает запросы в нескольких классах.</span><span class="sxs-lookup"><span data-stu-id="60d89-114">WQL does not support queries across multiple classes.</span></span>

<span data-ttu-id="60d89-115">СОЕДИНИТЕЛи и ссылки на инструкции относятся только к WQL и не являются частью стандартного SQL.</span><span class="sxs-lookup"><span data-stu-id="60d89-115">The ASSOCIATORS OF and REFERENCES OF statements are specific to WQL and are not part of standard SQL.</span></span> <span data-ttu-id="60d89-116">СОЕДИНИТЕЛи оператора получают все экземпляры классов, связанные с определенным экземпляром исходного класса, а ссылки на получение всех экземпляров, ссылающихся на конкретный экземпляр источника.</span><span class="sxs-lookup"><span data-stu-id="60d89-116">The ASSOCIATORS OF statement retrieves all class instances that are associated with a particular source class instance, and REFERENCES OF retrieves all instances that refer to a particular source instance.</span></span> <span data-ttu-id="60d89-117">Ассоциации представлены экземплярами [класса Association](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="60d89-117">Associations are represented by instances of an [association class](declaring-an-association-class.md).</span></span>

 

 



