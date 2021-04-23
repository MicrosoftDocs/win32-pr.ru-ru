---
description: Можно отфильтровать экземпляры класса представления соединений, назначив запрос WQL квалификатору Постжоинфилтер.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Квалификатор Постжоинфилтер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702659"
---
# <a name="postjoinfilter-qualifier"></a><span data-ttu-id="344bb-103">Квалификатор Постжоинфилтер</span><span class="sxs-lookup"><span data-stu-id="344bb-103">PostJoinFilter Qualifier</span></span>

<span data-ttu-id="344bb-104">Можно отфильтровать экземпляры класса представления соединений, назначив запрос WQL квалификатору **постжоинфилтер** .</span><span class="sxs-lookup"><span data-stu-id="344bb-104">You can filter the instances of a join view class by assigning a WQL query to the **PostJoinFilter** qualifier.</span></span> <span data-ttu-id="344bb-105">Значение WQL-запроса применяется к экземплярам класса представления JOIN.</span><span class="sxs-lookup"><span data-stu-id="344bb-105">The value of the WQL query is applied to the instances of the join view class.</span></span> <span data-ttu-id="344bb-106">Этот квалификатор можно использовать, чтобы ограничить экземпляры класса представления теми, которые соответствуют определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="344bb-106">You can use this qualifier to restrict the instances of your view class to those that meet specific conditions.</span></span> <span data-ttu-id="344bb-107">Следующий запрос WQL фильтрует экземпляры класса JOIN, вызываемые на основе экземпляров [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="344bb-107">The following WQL query filters instances of a join class called based on instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



<span data-ttu-id="344bb-108">Существует несколько ограничений на использование этого квалификатора.</span><span class="sxs-lookup"><span data-stu-id="344bb-108">There are several restrictions to the use of this qualifier:</span></span>

-   <span data-ttu-id="344bb-109">**Постжоинфилтер** доступен только для классов представлений JOIN.</span><span class="sxs-lookup"><span data-stu-id="344bb-109">**PostJoinFilter** is only available to join view classes.</span></span>
-   <span data-ttu-id="344bb-110">Имя класса и имена свойств, указанные в запросе, относятся к свойствам класса представления, а не к исходному классу.</span><span class="sxs-lookup"><span data-stu-id="344bb-110">The class name and property names specified in the query refer to the properties of the view class, not the source class.</span></span>
-   <span data-ttu-id="344bb-111">Исключение свойств не разрешено; допускаются только `SELECT *` запросы типа.</span><span class="sxs-lookup"><span data-stu-id="344bb-111">No exclusion of properties is permitted; only `SELECT *` type queries are allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="344bb-112">Требования</span><span class="sxs-lookup"><span data-stu-id="344bb-112">Requirements</span></span>



| <span data-ttu-id="344bb-113">Требование</span><span class="sxs-lookup"><span data-stu-id="344bb-113">Requirement</span></span> | <span data-ttu-id="344bb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="344bb-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="344bb-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="344bb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="344bb-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="344bb-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="344bb-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="344bb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="344bb-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="344bb-118">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="344bb-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="344bb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="344bb-120">**Квалификаторы, относящиеся к поставщику представления**</span><span class="sxs-lookup"><span data-stu-id="344bb-120">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

