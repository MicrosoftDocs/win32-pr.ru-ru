---
description: Установщик Windows выполняет следующие действия во время переустановки приложения, если пакет содержит изолированные компоненты. Обычно общий компонент \_ является библиотекой DLL, которая совместно используется приложениями-компонентами \_ и другими клиентскими исполняемыми файлами.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Повторная установка изолированных компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909447"
---
# <a name="reinstallation-of-isolated-components"></a><span data-ttu-id="e71cc-104">Повторная установка изолированных компонентов</span><span class="sxs-lookup"><span data-stu-id="e71cc-104">Reinstallation of Isolated Components</span></span>

<span data-ttu-id="e71cc-105">Установщик Windows выполняет следующие действия во время переустановки приложения, если пакет содержит изолированные компоненты.</span><span class="sxs-lookup"><span data-stu-id="e71cc-105">Windows Installer performs the following actions during reinstallation of an application when the package contains isolated components.</span></span> <span data-ttu-id="e71cc-106">Обычно общий компонент \_ является библиотекой DLL, которая совместно используется приложениями-компонентами \_ и другими клиентскими исполняемыми файлами.</span><span class="sxs-lookup"><span data-stu-id="e71cc-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="reinstallation"></a><span data-ttu-id="e71cc-107">переустановка;</span><span class="sxs-lookup"><span data-stu-id="e71cc-107">Reinstallation</span></span>

-   <span data-ttu-id="e71cc-108">Переустановка файлов компонента, \_ совместно используемых в той же папке, что и \_ приложение-компонент, только при повторной \_ установке приложения компонента.</span><span class="sxs-lookup"><span data-stu-id="e71cc-108">Reinstall of the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being reinstalled.</span></span>
-   <span data-ttu-id="e71cc-109">Не следует увеличивать список клиентов для общего доступа к компоненту \_ и не увеличивать счетчик шареддлл.</span><span class="sxs-lookup"><span data-stu-id="e71cc-109">Do not increment the client list of Component\_Shared and do not increment the SharedDLL count.</span></span>
-   <span data-ttu-id="e71cc-110">Повторно создайте нулевой байтовый файл с коротким именем файла ключа \_ приложения компонента.</span><span class="sxs-lookup"><span data-stu-id="e71cc-110">Recreate the zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="e71cc-111">Этот файл должен находиться в той же папке, что \_ и приложение компонента, и иметь расширение. Языковые.</span><span class="sxs-lookup"><span data-stu-id="e71cc-111">This file must be located in the same folder as Component\_Application and have the extension .LOCAL.</span></span>
-   <span data-ttu-id="e71cc-112">Переустановите все ресурсы компонентного \_ приложения, как обычно.</span><span class="sxs-lookup"><span data-stu-id="e71cc-112">Reinstall all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="e71cc-113">Если значение refcount Шареддлл для общего компонента больше \_ 1 или если другие продукты остаются в списке клиентов для общего доступа к компоненту \_ :</span><span class="sxs-lookup"><span data-stu-id="e71cc-113">If the SharedDLL refcount for Component\_Shared is more than 1, or if other products remain on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="e71cc-114">Переустановите файлы в общее расположение общего расположения компонента \_ .</span><span class="sxs-lookup"><span data-stu-id="e71cc-114">Reinstall no files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="e71cc-115">Если значение refcount Шареддлл для \_ общего компонента равно 1, или если другие оставшиеся клиенты компонента не имеют \_ общего доступа:</span><span class="sxs-lookup"><span data-stu-id="e71cc-115">If the SharedDLL refcount for Component\_Shared equals 1, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="e71cc-116">Переустановка файлов компонента, \_ совместно используемых в общем расположении, с использованием [правил управления версиями файлов](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="e71cc-116">Reinstall of the files of Component\_Shared into the shared location using the [File Versioning Rules](file-versioning-rules.md).</span></span>
-   <span data-ttu-id="e71cc-117">Обработать все действия по переустановке для \_ общего компонента.</span><span class="sxs-lookup"><span data-stu-id="e71cc-117">Process all reinstall actions for Component\_Shared.</span></span>
-   <span data-ttu-id="e71cc-118">Если компонент \_ Shared является COM-компонентом, зарегистрируйте полный путь com, чтобы синтаксис установщика \[ $Component \] и \[ \# филекэй \] указывал на общее расположение общего расположения компонента \_ .</span><span class="sxs-lookup"><span data-stu-id="e71cc-118">If Component\_Shared is a COM component, register the full COM path such that the installer syntaxes \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



