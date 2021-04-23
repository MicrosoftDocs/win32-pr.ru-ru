---
title: Моникеры файлов
description: Моникеры файлов
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329187"
---
# <a name="file-monikers"></a><span data-ttu-id="7dae0-103">Моникеры файлов</span><span class="sxs-lookup"><span data-stu-id="7dae0-103">File Monikers</span></span>

<span data-ttu-id="7dae0-104">*Моникеры файлов* — это простейший класс моникера.</span><span class="sxs-lookup"><span data-stu-id="7dae0-104">*File monikers* are the simplest moniker class.</span></span> <span data-ttu-id="7dae0-105">Моникеры файлов можно использовать для обнаружения любого объекта, хранящегося в его собственном файле.</span><span class="sxs-lookup"><span data-stu-id="7dae0-105">File monikers can be used to identify any object that is stored in its own file.</span></span> <span data-ttu-id="7dae0-106">Моникер файла выступает в качестве оболочки для имени пути, которую собственная файловая система назначает файлу.</span><span class="sxs-lookup"><span data-stu-id="7dae0-106">A file moniker acts as a wrapper for the path name the native file system assigns to the file.</span></span> <span data-ttu-id="7dae0-107">Вызов [**IMoniker:: биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) для этого моникера приведет к активации этого объекта, а затем вернет указатель интерфейса на объект.</span><span class="sxs-lookup"><span data-stu-id="7dae0-107">Calling [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) for this moniker would cause this object to be activated and then would return an interface pointer to the object.</span></span> <span data-ttu-id="7dae0-108">Источник объекта с именем моникера должен предоставлять реализацию интерфейса [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) для поддержки привязки моникера файла.</span><span class="sxs-lookup"><span data-stu-id="7dae0-108">The source of the object named by the moniker must provide an implementation of the [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) interface to support binding a file moniker.</span></span> <span data-ttu-id="7dae0-109">Моникеры файлов могут представлять собой полный или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="7dae0-109">File monikers can represent either a complete or a relative path.</span></span>

<span data-ttu-id="7dae0-110">Например, моникер файла для объекта электронной таблицы, хранящегося в файле C: \\ рабочий \\MySheet.xls, будет содержать сведения, эквивалентные этому пути.</span><span class="sxs-lookup"><span data-stu-id="7dae0-110">For example, the file moniker for a spreadsheet object stored as the file C:\\Work\\MySheet.xls would contain information equivalent to that path name.</span></span> <span data-ttu-id="7dae0-111">Однако моникер не обязательно должен состоять из одной и той же строки.</span><span class="sxs-lookup"><span data-stu-id="7dae0-111">The moniker would not necessarily consist of the same string, however.</span></span> <span data-ttu-id="7dae0-112">Строка — это просто *имя дисплайâ*, представление содержимого моникера, значимое для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="7dae0-112">The string is just its *displayÂ name*, a representation of the moniker's contents that is meaningful to an end user.</span></span> <span data-ttu-id="7dae0-113">Отображаемое имя, доступное через метод [**IMoniker::-DisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) , используется только при отображении моникера для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="7dae0-113">The display name, which is available through the [**IMoniker::GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) method, is used only when displaying a moniker to an end user.</span></span> <span data-ttu-id="7dae0-114">Этот метод получает отображаемое имя для любого класса моникера.</span><span class="sxs-lookup"><span data-stu-id="7dae0-114">This method gets the display name for any of the moniker classes.</span></span> <span data-ttu-id="7dae0-115">На внутреннем языке моникер может хранить одни и те же данные в формате, который более эффективен для выполнения операций моникера, но не имеет смысла для пользователей.</span><span class="sxs-lookup"><span data-stu-id="7dae0-115">Internally, the moniker may store the same information in a format that is more efficient for performing moniker operations but isn't meaningful to users.</span></span> <span data-ttu-id="7dae0-116">Затем, если этот же объект привязан через вызов метода [**биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) , объект будет активирован, возможно, путем загрузки файла в электронную таблицу.</span><span class="sxs-lookup"><span data-stu-id="7dae0-116">Then, when this same object is bound through a call to the [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) method, the object would be activated, probably by loading the file into the spreadsheet.</span></span>

<span data-ttu-id="7dae0-117">OLE предлагает поставщики моникеров, вспомогательная функция [**креатефилемоникер**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) , которая создает объект моникера файла и возвращает указатель на поставщик.</span><span class="sxs-lookup"><span data-stu-id="7dae0-117">OLE offers moniker providers the helper function [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) that creates a file moniker object and returns its pointer to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dae0-118">См. также</span><span class="sxs-lookup"><span data-stu-id="7dae0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dae0-119">Специальные имена</span><span class="sxs-lookup"><span data-stu-id="7dae0-119">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="7dae0-120">Моникеры класса</span><span class="sxs-lookup"><span data-stu-id="7dae0-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="7dae0-121">Составные моникеры</span><span class="sxs-lookup"><span data-stu-id="7dae0-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="7dae0-122">Моникеры элементов</span><span class="sxs-lookup"><span data-stu-id="7dae0-122">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="7dae0-123">Моникеры указателей</span><span class="sxs-lookup"><span data-stu-id="7dae0-123">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




