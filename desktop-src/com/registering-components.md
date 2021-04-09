---
title: Регистрация компонентов
description: Регистрация компонентов
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070661"
---
# <a name="registering-components"></a><span data-ttu-id="42484-103">Регистрация компонентов</span><span class="sxs-lookup"><span data-stu-id="42484-103">Registering Components</span></span>

<span data-ttu-id="42484-104">При установке следующих типов приложений сведения об установке должны быть добавлены в реестр, обычно через программу установки:</span><span class="sxs-lookup"><span data-stu-id="42484-104">When the following types of applications are installed, installation information must be added to the registry, usually through a setup program:</span></span>

-   <span data-ttu-id="42484-105">Серверные приложения</span><span class="sxs-lookup"><span data-stu-id="42484-105">Server applications</span></span>
-   <span data-ttu-id="42484-106">Приложения-контейнеры и серверы</span><span class="sxs-lookup"><span data-stu-id="42484-106">Container/server applications</span></span>
-   <span data-ttu-id="42484-107">Приложения контейнеров, разрешающие связывание с внедренными объектами</span><span class="sxs-lookup"><span data-stu-id="42484-107">Container applications that allow linking to embedded objects</span></span>

<span data-ttu-id="42484-108">Для всех трех экземпляров Зарегистрируйте сведения о библиотеке COM (DLL) и сведения о конкретном приложении.</span><span class="sxs-lookup"><span data-stu-id="42484-108">For all three instances, register COM library (DLL) information and application-specific information.</span></span>

<span data-ttu-id="42484-109">Библиотека DLL регистрирует сведения для всех своих компонентов путем экспорта [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="42484-109">The DLL registers the information for all its components by exporting [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="42484-110">Используйте следующие функции для регистрации и отмены регистрации компонента:</span><span class="sxs-lookup"><span data-stu-id="42484-110">Use the following functions to register and unregister a component:</span></span>

-   [<span data-ttu-id="42484-111">**RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="42484-111">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [<span data-ttu-id="42484-112">**регкреатекэйекс**</span><span class="sxs-lookup"><span data-stu-id="42484-112">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="42484-113">**RegSetValueEx**</span><span class="sxs-lookup"><span data-stu-id="42484-113">**RegSetValueEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [<span data-ttu-id="42484-114">**реженумкэйекс**</span><span class="sxs-lookup"><span data-stu-id="42484-114">**RegEnumKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [<span data-ttu-id="42484-115">**регделетекэй**</span><span class="sxs-lookup"><span data-stu-id="42484-115">**RegDeleteKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [<span data-ttu-id="42484-116">**Ошибка RegCloseKey**</span><span class="sxs-lookup"><span data-stu-id="42484-116">**RegCloseKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a><span data-ttu-id="42484-117">См. также</span><span class="sxs-lookup"><span data-stu-id="42484-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42484-118">Регистрация приложений COM</span><span class="sxs-lookup"><span data-stu-id="42484-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 