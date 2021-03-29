---
description: Установщик Windows выполняет следующие действия во время установки приложения, если пакет содержит изолированные компоненты. Обычно общий компонент \_ является библиотекой DLL, которая совместно используется приложениями-компонентами \_ и другими клиентскими исполняемыми файлами.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Установка изолированных компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811476"
---
# <a name="installation-of-isolated-components"></a><span data-ttu-id="40cc9-104">Установка изолированных компонентов</span><span class="sxs-lookup"><span data-stu-id="40cc9-104">Installation of Isolated Components</span></span>

<span data-ttu-id="40cc9-105">Установщик Windows выполняет следующие действия во время установки приложения, если пакет содержит изолированные компоненты.</span><span class="sxs-lookup"><span data-stu-id="40cc9-105">Windows Installer performs the following actions during installation of an application when the package contains isolated components.</span></span> <span data-ttu-id="40cc9-106">Обычно общий компонент \_ является библиотекой DLL, которая совместно используется приложениями-компонентами \_ и другими клиентскими исполняемыми файлами.</span><span class="sxs-lookup"><span data-stu-id="40cc9-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="installation"></a><span data-ttu-id="40cc9-107">Установка</span><span class="sxs-lookup"><span data-stu-id="40cc9-107">Installation</span></span>

-   <span data-ttu-id="40cc9-108">Скопируйте файлы компонента \_ , общие в ту же папку, что и \_ приложение компонента, только если \_ также устанавливается приложение компонента.</span><span class="sxs-lookup"><span data-stu-id="40cc9-108">Copy the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being installed.</span></span>
-   <span data-ttu-id="40cc9-109">Создайте нулевой байтовый файл с коротким именем файла ключа \_ приложения компонента.</span><span class="sxs-lookup"><span data-stu-id="40cc9-109">Create a zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="40cc9-110">Нахождение этого файла в той же папке, что и \_ приложение компонента.</span><span class="sxs-lookup"><span data-stu-id="40cc9-110">Locate this file in the same folder as Component\_Application.</span></span> <span data-ttu-id="40cc9-111">Добавьте расширение. ЛОКАЛЬНЫЙ с этим именем файла.</span><span class="sxs-lookup"><span data-stu-id="40cc9-111">Append the extension .LOCAL to this file name.</span></span>
-   <span data-ttu-id="40cc9-112">Увеличьте значение refcount Шареддлл, если бит Мсидбкомпонентаттрибутесшареддллрефкаунт установлен в столбце Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="40cc9-112">Increment the SharedDLL refcount if the msidbComponentAttributesSharedDllRefCount bit is set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="40cc9-113">Регистрация \_ приложения-компонента в качестве клиента \_ общего компонента и регистрация пути к ключу, указывающего на общее расположение общего расположения компонента \_ .</span><span class="sxs-lookup"><span data-stu-id="40cc9-113">Register Component\_Application as a client of Component\_Shared and register a key path pointing to the shared location of Component\_Shared.</span></span>
-   <span data-ttu-id="40cc9-114">Установите все ресурсы компонентного \_ приложения обычным образом.</span><span class="sxs-lookup"><span data-stu-id="40cc9-114">Install all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="40cc9-115">Если \_ общий доступ к компоненту или его файл ключа уже установлен на компьютере, не копируйте файлы в общее расположение общего расположения компонента \_ .</span><span class="sxs-lookup"><span data-stu-id="40cc9-115">If Component\_Shared or its key file is already installed on the computer do not copy files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="40cc9-116">Если \_ общий компонент или его файл ключа еще не установлены на компьютере:</span><span class="sxs-lookup"><span data-stu-id="40cc9-116">If Component\_Shared or its key file is not yet installed on the computer:</span></span>

-   <span data-ttu-id="40cc9-117">Скопируйте файлы компонента, \_ совместно используемые в общем расположении.</span><span class="sxs-lookup"><span data-stu-id="40cc9-117">Copy the files of Component\_Shared to the shared location.</span></span>
-   <span data-ttu-id="40cc9-118">Обработать все действия по установке для \_ общего компонента.</span><span class="sxs-lookup"><span data-stu-id="40cc9-118">Process all install actions for Component\_Shared.</span></span>
-   <span data-ttu-id="40cc9-119">Если компонент \_ Shared является COM-компонентом, зарегистрируйте полный путь com, \[ чтобы синтаксис $Component \] и \[ \# филекэй \] указывал на общее расположение общего расположения компонента \_ .</span><span class="sxs-lookup"><span data-stu-id="40cc9-119">If Component\_Shared is a COM component, register the full COM path such that the syntax \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



