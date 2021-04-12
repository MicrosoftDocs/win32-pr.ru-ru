---
title: Моникеры класса
description: Хотя классы обычно идентифицируются непосредственно с идентификаторами CLSID для таких функций, как CoCreateInstance или Кожетклассобжект, теперь классы также могут быть идентифицированы с помощью моникера, называемого моникером класса.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80886ce49ea25d2fb5acbf4dddf550c9d2c3ae29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332195"
---
# <a name="class-monikers"></a><span data-ttu-id="00cd6-103">Моникеры класса</span><span class="sxs-lookup"><span data-stu-id="00cd6-103">Class Monikers</span></span>

<span data-ttu-id="00cd6-104">Хотя классы обычно идентифицируются непосредственно с идентификаторами CLSID для таких функций, как [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) или [**кожетклассобжект**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), теперь классы также могут быть идентифицированы с помощью моникера, называемого *моникером класса*.</span><span class="sxs-lookup"><span data-stu-id="00cd6-104">Although classes are typically identified directly with CLSIDs to functions such as [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), classes may also now be identified with a moniker called a *class moniker*.</span></span> <span data-ttu-id="00cd6-105">Моникеры класса привязываются к объекту класса класса, для которого они созданы.</span><span class="sxs-lookup"><span data-stu-id="00cd6-105">Class monikers bind to the class object of the class for which they are created.</span></span>

<span data-ttu-id="00cd6-106">Возможность определять классы с моникером поддерживает полезные операции, которые в противном случае являются неудобными.</span><span class="sxs-lookup"><span data-stu-id="00cd6-106">The ability to identify classes with a moniker supports useful operations that are otherwise unwieldy.</span></span> <span data-ttu-id="00cd6-107">Например, моникеры файлов традиционно поддерживали широкие возможности привязки только к классу, связанному с классом файла, на который они ссылаются; моникер для файла Excel привязывается к экземпляру объекта Excel, а моникер для изображения GIF привязывается к экземпляру текущего зарегистрированного обработчика GIF.</span><span class="sxs-lookup"><span data-stu-id="00cd6-107">For example, file monikers traditionally supported rich binding only to the class associated with the class of file they referred to; a moniker to an Excel file would bind to an instance of an Excel object, and a moniker to a GIF image would bind to an instance of the currently registered GIF handler.</span></span> <span data-ttu-id="00cd6-108">Моникер класса позволяет указать класс, который вы хотите использовать для управления файлом через композицию с моникером файла.</span><span class="sxs-lookup"><span data-stu-id="00cd6-108">A class moniker allows you to indicate the class you want to use to manipulate a file through composition with a file moniker.</span></span> <span data-ttu-id="00cd6-109">Моникер класса для класса трехмерной диаграммы, состоящий из моникера для файла Excel, выдает моникер, который привязывается к экземпляру трехмерного объекта диаграммы и инициализирует объект с содержимым файла Excel.</span><span class="sxs-lookup"><span data-stu-id="00cd6-109">A class moniker for a 3D charting class composed with a moniker to an Excel file yields a moniker that binds to an instance of the 3D charting object and initializes the object with the contents of the Excel file.</span></span>

<span data-ttu-id="00cd6-110">Таким образом, моникеры классов наиболее полезны в композиции с другими типами моникеров, такими как моникеры файлов или моникеры элементов.</span><span class="sxs-lookup"><span data-stu-id="00cd6-110">Class monikers are therefore most useful in composition with other types of monikers, such as file monikers or item monikers.</span></span>

<span data-ttu-id="00cd6-111">Моникеры класса также могут состоять из имен справа от моникеров, поддерживающих привязку к интерфейсу [**иклассактиватор**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) .</span><span class="sxs-lookup"><span data-stu-id="00cd6-111">Class monikers may also be composed to the right of monikers supporting binding to the [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) interface.</span></span> <span data-ttu-id="00cd6-112">При этом **иклассактиватор** просто предоставляет доступ к объекту класса и экземплярам класса через [**Иклассактиватор:: жетклассобжект**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span><span class="sxs-lookup"><span data-stu-id="00cd6-112">When composed in this manner, **IClassActivator** simply gives access to the class object and instances of the class through [**IClassActivator::GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span></span> <span data-ttu-id="00cd6-113">Моникеры класса можно определить с помощью [**IMoniker:: иссистеммоникер**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), который возвращает мксис \_ классмоникер в *пдвмксис*.</span><span class="sxs-lookup"><span data-stu-id="00cd6-113">Class monikers may be identified through [**IMoniker::IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), which returns MKSYS\_CLASSMONIKER in *pdwMksys*.</span></span>

<span data-ttu-id="00cd6-114">Программисты обычно создают моникеры классов с помощью функции [**креатеклассмоникер**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) или [**мкпарседисплайнаме**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span><span class="sxs-lookup"><span data-stu-id="00cd6-114">Programmers typically create class monikers using the [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) function or through [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span></span> <span data-ttu-id="00cd6-115">(Дополнительные сведения см. в разделе [**IMoniker::P арседисплайнаме**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) .)</span><span class="sxs-lookup"><span data-stu-id="00cd6-115">(See [**IMoniker::ParseDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) for details.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="00cd6-116">См. также</span><span class="sxs-lookup"><span data-stu-id="00cd6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00cd6-117">Специальные имена</span><span class="sxs-lookup"><span data-stu-id="00cd6-117">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="00cd6-118">Составные моникеры</span><span class="sxs-lookup"><span data-stu-id="00cd6-118">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="00cd6-119">Моникеры файлов</span><span class="sxs-lookup"><span data-stu-id="00cd6-119">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="00cd6-120">Моникеры элементов</span><span class="sxs-lookup"><span data-stu-id="00cd6-120">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="00cd6-121">Моникеры указателей</span><span class="sxs-lookup"><span data-stu-id="00cd6-121">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




