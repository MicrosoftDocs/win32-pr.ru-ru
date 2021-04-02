---
title: Синтаксис имени
description: Синтаксис удаленного вызова процедур (RPC) и имени.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d024130a5b8a873c6bfbb2194542344953625d5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986659"
---
# <a name="name-syntax"></a><span data-ttu-id="716a4-103">Синтаксис имени</span><span class="sxs-lookup"><span data-stu-id="716a4-103">Name Syntax</span></span>

<span data-ttu-id="716a4-104">Microsoft RPC принимает имена, соответствующие следующему синтаксису:</span><span class="sxs-lookup"><span data-stu-id="716a4-104">Microsoft RPC accepts names that conform to the following syntax:</span></span>

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a><span data-ttu-id="716a4-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="716a4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="716a4-106"><span id="name"></span><span id="NAME"></span>безымян</span><span class="sxs-lookup"><span data-stu-id="716a4-106"><span id="name"></span><span id="NAME"></span>name</span></span>
</dt> <dd>

<span data-ttu-id="716a4-107">Указывает идентификатор, который может содержать любой символ, кроме символа косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="716a4-107">Specifies an identifier that can contain any character except the delimiting slash (/) character.</span></span>

</dd> <dt>

<span data-ttu-id="716a4-108"><span id="domainname"></span><span id="DOMAINNAME"></span>имя_домена</span><span class="sxs-lookup"><span data-stu-id="716a4-108"><span id="domainname"></span><span id="DOMAINNAME"></span>domainname</span></span>
</dt> <dd>

<span data-ttu-id="716a4-109">Указывает имя домена.</span><span class="sxs-lookup"><span data-stu-id="716a4-109">Specifies the name of the domain.</span></span>

</dd> </dl>

<span data-ttu-id="716a4-110">Параметр, выбирающий тип синтаксиса Name-Syntax, и строка, указывающая имя, предоставляются многим функциям RPC с интерфейсом службы имен (NSI).</span><span class="sxs-lookup"><span data-stu-id="716a4-110">A parameter that selects the name-syntax type and the string that specifies the name are supplied to many of the name service interface (NSI) RPC functions.</span></span>

<span data-ttu-id="716a4-111">В Microsoft RPC поддерживается только один тип синтаксиса имени, который указывается константой RPC \_ C NS с \_ \_ синтаксисом \_ DCE.</span><span class="sxs-lookup"><span data-stu-id="716a4-111">Only one name-syntax type is supported by Microsoft RPC, as specified by the constant RPC\_C\_NS\_SYNTAX\_DCE.</span></span> <span data-ttu-id="716a4-112">Эта константа определена в файле заголовка РПКНСИ. H.</span><span class="sxs-lookup"><span data-stu-id="716a4-112">This constant is defined in the header file RPCNSI.H.</span></span>

<span data-ttu-id="716a4-113">Синтаксис имени, заданный с \_ помощью \_ синтаксиса RPC C NS, \_ \_ является расширением \_ синтаксиса имени службы каталога ячеек использование DCE (CD).</span><span class="sxs-lookup"><span data-stu-id="716a4-113">The name syntax specified by RPC\_C\_NS\_SYNTAX\_DCE is an extension of the OSF\_DCE Cell Directory Service (CDS) name syntax.</span></span> <span data-ttu-id="716a4-114">Возможность указания имени домена представляет собой расширение для этого синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="716a4-114">The ability to specify a domain name represents an extension to that syntax.</span></span> <span data-ttu-id="716a4-115">Не существует абсолютного ограничения на количество имен, которые могут быть разделены символами косой черты, если общая строка содержит менее 256 символов.</span><span class="sxs-lookup"><span data-stu-id="716a4-115">There is no absolute limit on the number of names that can be separated by slash characters as long as the overall string is less than 256 characters.</span></span>

<span data-ttu-id="716a4-116">Косые черты позволяют указать в имени логическую структуру, но они не соответствуют логической структуре самих объектов.</span><span class="sxs-lookup"><span data-stu-id="716a4-116">The slashes allow you to specify a logical structure to the name, but they do not correspond to a logical structure in the objects themselves.</span></span>

 

 




