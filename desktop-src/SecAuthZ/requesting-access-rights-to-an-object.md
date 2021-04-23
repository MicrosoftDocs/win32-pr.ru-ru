---
description: При открытии обработчика для объекта возвращенный обработчик имеет некоторую комбинацию прав доступа к объекту.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Запрос прав доступа к объекту
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662571"
---
# <a name="requesting-access-rights-to-an-object"></a><span data-ttu-id="b0adf-103">Запрос прав доступа к объекту</span><span class="sxs-lookup"><span data-stu-id="b0adf-103">Requesting Access Rights to an Object</span></span>

<span data-ttu-id="b0adf-104">При открытии обработчика для объекта возвращенный обработчик имеет некоторую комбинацию прав доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="b0adf-104">When you open a handle to an object, the returned handle has some combination of access rights to the object.</span></span> <span data-ttu-id="b0adf-105">Для некоторых функций, таких как [**createsemaphore-**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), не требуется определенный набор запрошенных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="b0adf-105">Some functions, such as [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), do not require a specific set of requested access rights.</span></span> <span data-ttu-id="b0adf-106">Эти функции всегда пытаются открыть маркер для полного доступа.</span><span class="sxs-lookup"><span data-stu-id="b0adf-106">These functions always try to open the handle for full access.</span></span> <span data-ttu-id="b0adf-107">Другие функции, такие как [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) и [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), позволяют указать необходимый набор прав доступа.</span><span class="sxs-lookup"><span data-stu-id="b0adf-107">Other functions, such as [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), allow you to specify the set of access rights that you want.</span></span> <span data-ttu-id="b0adf-108">Следует запрашивать только необходимые права доступа, а не открывать полный доступ.</span><span class="sxs-lookup"><span data-stu-id="b0adf-108">You should request only the access rights that you need, rather than opening a handle for full access.</span></span> <span data-ttu-id="b0adf-109">Это предотвращает непреднамеренное использование этого маркера и увеличивает вероятность того, что запрос доступа будет выполнен, если DACL объекта допускает только ограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="b0adf-109">This prevents using the handle in an unintended way, and increases the chances that the access request will succeed if the object's DACL only allows limited access.</span></span>

<span data-ttu-id="b0adf-110">Используйте [универсальные права доступа](generic-access-rights.md) , чтобы указать тип доступа, необходимый при открытии маркера для объекта.</span><span class="sxs-lookup"><span data-stu-id="b0adf-110">Use [generic access rights](generic-access-rights.md) to specify the type of access needed when opening a handle to an object.</span></span> <span data-ttu-id="b0adf-111">Обычно это проще, чем указывать все соответствующие стандартные и специальные права.</span><span class="sxs-lookup"><span data-stu-id="b0adf-111">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span> <span data-ttu-id="b0adf-112">Кроме того, используйте максимально \_ допустимую константу, чтобы запросить открытие объекта со всеми правами доступа, которые являются допустимыми для вызывающего.</span><span class="sxs-lookup"><span data-stu-id="b0adf-112">Alternatively, use the MAXIMUM\_ALLOWED constant to request that the object be opened with all the access rights that are valid for the caller.</span></span>

> [!Note]  
> <span data-ttu-id="b0adf-113">МАКСИМАЛЬНО \_ допустимую константу нельзя использовать в элементе управления доступом.</span><span class="sxs-lookup"><span data-stu-id="b0adf-113">The MAXIMUM\_ALLOWED constant cannot be used in an ACE.</span></span>

 

<span data-ttu-id="b0adf-114">Чтобы получить или задать список SACL в [*дескрипторе безопасности*](/windows/desktop/SecGloss/s-gly)объекта, запросите [ \_ право доступа системы доступа \_ безопасности](sacl-access-right.md) при открытии дескриптора объекта.</span><span class="sxs-lookup"><span data-stu-id="b0adf-114">To get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), request the [ACCESS\_SYSTEM\_SECURITY access right](sacl-access-right.md) when opening a handle to the object.</span></span>

 

 
