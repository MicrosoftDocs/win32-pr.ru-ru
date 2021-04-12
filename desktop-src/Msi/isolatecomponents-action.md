---
description: Действие Исолатекомпонентс устанавливает копию компонента (обычно это общая библиотека DLL) в частное расположение для использования конкретным приложением (обычно это exe-файл).
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Действие Исолатекомпонентс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348982"
---
# <a name="isolatecomponents-action"></a><span data-ttu-id="d15b7-103">Действие Исолатекомпонентс</span><span class="sxs-lookup"><span data-stu-id="d15b7-103">IsolateComponents Action</span></span>

<span data-ttu-id="d15b7-104">Действие Исолатекомпонентс устанавливает копию компонента (обычно это общая библиотека DLL) в частное расположение для использования конкретным приложением (обычно это exe-файл).</span><span class="sxs-lookup"><span data-stu-id="d15b7-104">The IsolateComponents action installs a copy of a component (commonly a shared DLL) into a private location for use by a specific application (typically an .exe).</span></span> <span data-ttu-id="d15b7-105">Это позволяет изолировать приложение от других копий компонента, которые могут быть установлены в общую папку на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d15b7-105">This isolates the application from other copies of the component that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="d15b7-106">Дополнительные сведения см. в разделе [изолированные компоненты](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="d15b7-106">For more information, see [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="d15b7-107">Действие ссылается на каждую запись [таблицы исолатедкомпонент](isolatedcomponent-table.md) и связывает файлы компонента, перечисленные в \_ общем поле Component, с компонентом, указанным в \_ поле приложение компонента.</span><span class="sxs-lookup"><span data-stu-id="d15b7-107">The action refers to each record of the [IsolatedComponent table](isolatedcomponent-table.md) and associates the files of the component listed in the Component\_Shared field with the component listed in the Component\_Application field.</span></span> <span data-ttu-id="d15b7-108">Установщик устанавливает файлы компонента, \_ совместно используемые в том же каталоге, что и \_ приложение компонента.</span><span class="sxs-lookup"><span data-stu-id="d15b7-108">The installer installs the files of Component\_Shared into the same directory as Component\_Application.</span></span> <span data-ttu-id="d15b7-109">Установщик создает файл в этом каталоге, нулевое значение длины, наличие короткого имени файла ключа для \_ приложения компонента (как правило, это то же имя файла, что и exe-файл), добавленного с помощью. local.</span><span class="sxs-lookup"><span data-stu-id="d15b7-109">The installer generates a file in this directory, zero bytes in length, having the short filename name of the key file for Component\_Application (typically this is the same file name as the .exe) appended with .local.</span></span> <span data-ttu-id="d15b7-110">Действие Исолатедкомпонент не влияет на установку \_ приложения компонента.</span><span class="sxs-lookup"><span data-stu-id="d15b7-110">The IsolatedComponent action does not affect the installation of Component\_Application.</span></span> <span data-ttu-id="d15b7-111">При удалении приложения компонента \_ также удаляются \_ Общие файлы компонента и локальный файл из каталога.</span><span class="sxs-lookup"><span data-stu-id="d15b7-111">Uninstalling Component\_Application also removes the Component\_Shared files and the .local file from the directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d15b7-112">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="d15b7-112">Sequence Restrictions</span></span>

<span data-ttu-id="d15b7-113">Действие Исолатекомпонентс может использоваться только в [таблицах инсталлуисекуенце](installuisequence-table.md) и [инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="d15b7-113">The IsolateComponents action can be used only in the [InstallUISequence table](installuisequence-table.md) and the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="d15b7-114">Это действие должно следовать после [действия костинитиализе](costinitialize-action.md) и перед [действием костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="d15b7-114">This action must come after the [CostInitialize action](costinitialize-action.md) and before the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d15b7-115">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="d15b7-115">ActionData Messages</span></span>

<span data-ttu-id="d15b7-116">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="d15b7-116">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="d15b7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d15b7-117">Remarks</span></span>

<span data-ttu-id="d15b7-118">Если столбец условия для действия Исолатекомпонентс равен true или оставлен пустым, установщик изолирует все компоненты, перечисленные в [таблице исолатедкомпонент](isolatedcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="d15b7-118">If the Condition column for the IsolateComponents action evaluates to True, or is left blank, the installer isolates all the components listed in the [IsolatedComponent table](isolatedcomponent-table.md).</span></span> <span data-ttu-id="d15b7-119">Если столбец Condition имеет значение false, установщик игнорирует таблицу Исолатедкомпонент и использует обычные компоненты.</span><span class="sxs-lookup"><span data-stu-id="d15b7-119">If the Condition column evaluates to False, the installer ignores the IsolatedComponent table and shares the components usual.</span></span> <span data-ttu-id="d15b7-120">Для условия этого действия можно использовать свойство [**редиректеддллсуппорт**](redirecteddllsupport.md) .</span><span class="sxs-lookup"><span data-stu-id="d15b7-120">The [**RedirectedDllSupport**](redirecteddllsupport.md) property may be used to condition this action.</span></span> <span data-ttu-id="d15b7-121">Дополнительные сведения см. в разделе [Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="d15b7-121">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



