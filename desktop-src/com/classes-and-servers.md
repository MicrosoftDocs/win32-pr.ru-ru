---
title: Классы и серверы
description: Классы и серверы
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413836"
---
# <a name="classes-and-servers"></a><span data-ttu-id="e3f15-103">Классы и серверы</span><span class="sxs-lookup"><span data-stu-id="e3f15-103">Classes and Servers</span></span>

<span data-ttu-id="e3f15-104">COM использует **\_ \_ корневые классы hKey** для параметров на уровне компьютера, но также позволяет настраивать идентификаторы CLSID для каждого пользователя для повышения безопасности и гибкости.</span><span class="sxs-lookup"><span data-stu-id="e3f15-104">COM uses **HKEY\_CLASSES\_ROOT** for computer-wide settings but also allows per-user configuration of CLSIDS for greater security and flexibility.</span></span> <span data-ttu-id="e3f15-105">Сначала модель COM обращается к **\_ \_ \\ \\ классам текущего пользовательского программного обеспечения hKey** , прежде чем искать их в **\_ \_ корне классов hKey**.</span><span class="sxs-lookup"><span data-stu-id="e3f15-105">COM first consults **HKEY\_CURRENT\_USER\\Software\\Classes** before looking under **HKEY\_CLASSES\_ROOT**.</span></span> <span data-ttu-id="e3f15-106">COM хранит сведения о компьютере, относящиеся к CLSID в **\_ \_ корневом \\ CLSID классов hKey** , и сохраняет сведения о классе для каждого пользователя в разделе **hKey \_ Current \_ user \\ Software \\ Classes \\ CLSID**.</span><span class="sxs-lookup"><span data-stu-id="e3f15-106">COM keeps computer-wide information related to CLSIDs under **HKEY\_CLASSES\_ROOT\\CLSID** and keeps per-user class information under **HKEY\_CURRENT\_USER\\Software\\Classes\\CLSID**.</span></span>

<span data-ttu-id="e3f15-107">Серверы COM поддерживают самостоятельную регистрацию.</span><span class="sxs-lookup"><span data-stu-id="e3f15-107">COM servers support self-registration.</span></span> <span data-ttu-id="e3f15-108">Для внутрипроцессного сервера это означает, что библиотека DLL должна экспортировать следующие функции:</span><span class="sxs-lookup"><span data-stu-id="e3f15-108">For an in-process server, this means that the DLL must export the following functions:</span></span>

-   [<span data-ttu-id="e3f15-109">**Регистрация**</span><span class="sxs-lookup"><span data-stu-id="e3f15-109">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [<span data-ttu-id="e3f15-110">**DllUnregisterServer**</span><span class="sxs-lookup"><span data-stu-id="e3f15-110">**DllUnregisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

<span data-ttu-id="e3f15-111">Эти функции необходимо экспортировать явным образом с помощью файла определения модуля, переключателей компоновщика или директив компилятора.</span><span class="sxs-lookup"><span data-stu-id="e3f15-111">You must explicitly export these functions by using a module definition file, linker switches, or compiler directives.</span></span> <span data-ttu-id="e3f15-112">Хранилище классов использует эти функции для настройки локального реестра после загрузки файла на клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="e3f15-112">The class store uses these functions to configure the local registry after downloading the file to the client machine.</span></span> <span data-ttu-id="e3f15-113">В дополнение к хранилищу классов эти функции также используются другими средами для установки серверов на ведущих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="e3f15-113">In addition to class store, these functions are also used by other environments to install servers on host computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3f15-114">См. также</span><span class="sxs-lookup"><span data-stu-id="e3f15-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3f15-115">Регистрация приложений COM</span><span class="sxs-lookup"><span data-stu-id="e3f15-115">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 