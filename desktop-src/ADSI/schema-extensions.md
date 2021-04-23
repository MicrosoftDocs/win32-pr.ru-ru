---
title: Расширения схемы
description: Архитектура схемы ADSI предоставляет возможность добавления новых классов схемы в контейнер класса схемы и новых свойств в существующий объект класса схемы во время выполнения.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b86491966e2bfddbef72d68d7a96869448c38188
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132790"
---
# <a name="schema-extensions"></a><span data-ttu-id="01e32-103">Расширения схемы</span><span class="sxs-lookup"><span data-stu-id="01e32-103">Schema Extensions</span></span>

<span data-ttu-id="01e32-104">Архитектура схемы ADSI предоставляет возможность добавления новых классов схемы в контейнер класса схемы и новых свойств в существующий объект класса схемы во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="01e32-104">The architecture of the ADSI schema provides that new schema classes can be added to the schema class container and new properties to an existing schema class object at run time.</span></span> <span data-ttu-id="01e32-105">Последняя возможность не требует нового кода.</span><span class="sxs-lookup"><span data-stu-id="01e32-105">The latter ability requires no new code.</span></span> <span data-ttu-id="01e32-106">Это важная функция для пространств имен, которые позволяют использовать расширяемые службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="01e32-106">This is an important feature for namespaces that allow extensible directory services.</span></span> <span data-ttu-id="01e32-107">Компонент поставщика должен разрешать эту расширяемость и иметь возможность получать доступ к экземпляру класса и значения его свойств и сохранять их.</span><span class="sxs-lookup"><span data-stu-id="01e32-107">The provider component must allow for this extensibility and know where to access and store the class instance and the values of its properties.</span></span> <span data-ttu-id="01e32-108">В типичной расширяемой службе каталогов эти сведения хранятся в базе данных службы каталогов так же, как и любые другие определения классов и свойств схемы.</span><span class="sxs-lookup"><span data-stu-id="01e32-108">In a typical extensible directory service, this information is stored in the directory service database in the same manner as any other schema class and property definitions.</span></span>

> [!Note]  
> <span data-ttu-id="01e32-109">В терминологии COM-интерфейса в существующий класс схемы можно добавлять только свойства, а не методы.</span><span class="sxs-lookup"><span data-stu-id="01e32-109">In COM interface terminology, only properties can be added to an existing schema class, not methods.</span></span> <span data-ttu-id="01e32-110">Добавление нового метода потребует добавления новой реализации этого метода и, таким образом, требует дополнительного кода.</span><span class="sxs-lookup"><span data-stu-id="01e32-110">Adding a new method would require adding a new implementation of that method and thus require additional code.</span></span>

 

<span data-ttu-id="01e32-111">Пример схемы конкретного поставщика см. в разделе [Управление схемой](schema-management.md).</span><span class="sxs-lookup"><span data-stu-id="01e32-111">For an example of a specific provider schema, see [Schema Management](schema-management.md).</span></span>

 

 




