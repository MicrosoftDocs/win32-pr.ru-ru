---
title: Объекты данных сервера
description: API серверных объектов данных (SDO) позволяет программно настраивать и администрировать систему, на которой выполняется NPS.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672331"
---
# <a name="server-data-objects"></a><span data-ttu-id="2ed7e-103">Объекты данных сервера</span><span class="sxs-lookup"><span data-stu-id="2ed7e-103">Server Data Objects</span></span>

> [!Note]  
> <span data-ttu-id="2ed7e-104">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="2ed7e-105">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="2ed7e-106">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="2ed7e-107">API серверных объектов данных (SDO) позволяет программно настраивать и администрировать систему, на которой выполняется NPS.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-107">The Server Data Objects (SDO) API makes it possible to programmatically configure and administer a system running NPS.</span></span> <span data-ttu-id="2ed7e-108">С помощью SDO разработчик может также создавать приложения, которые управляют политиками и профилями удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-108">Using SDO, a developer can also write applications that administer remote access policies and profiles.</span></span> <span data-ttu-id="2ed7e-109">Политики и профили удаленного доступа используются службой маршрутизации и удаленного доступа (RRAS), а также NPS, чтобы определить, разрешено ли удаленному клиенту подключаться к серверу доступа к сети (NAS).</span><span class="sxs-lookup"><span data-stu-id="2ed7e-109">The remote access policies and profiles are used by the Routing and Remote Access Service (RRAS) as well as NPS to determine whether a remote client is allowed to connect to a network access server (NAS).</span></span>

<span data-ttu-id="2ed7e-110">API SDO применим в любой среде, использующей NPS или политики удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-110">The SDO API is applicable in any environment that uses NPS or Remote Access Policies.</span></span>

<span data-ttu-id="2ed7e-111">С помощью API SDO разработчик может управлять любым элементом конфигурации NPS, доступ к которому можно получить через пользовательский интерфейс NPS.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-111">With the SDO API, a developer can manipulate any element of the NPS configuration that is accessible through the NPS user interface.</span></span>

<span data-ttu-id="2ed7e-112">API SDO также позволяет задавать или извлекать любые значения, доступные на странице свойств параметры коммутируемого подключения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-112">The SDO API also makes it possible to set or retrieve any of the values accessible through the user dial-in settings property page.</span></span>

<span data-ttu-id="2ed7e-113">API SDO состоит из COM-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-113">The SDO API is composed of COM interfaces.</span></span> <span data-ttu-id="2ed7e-114">Каждый интерфейс в API SDO наследует от интерфейса COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="2ed7e-114">Each of the interfaces in the SDO API inherits from the COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="2ed7e-115">Интерфейс **IDispatch** позволяет разработчикам вызывать методы интерфейса SDO из Visual Basic или любого клиента автоматизации, а также из C/C++.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-115">The **IDispatch** interface enables developers to call the SDO interface methods from Visual Basic or any Automation client, as well as from C/C++.</span></span>

<span data-ttu-id="2ed7e-116">Разработчики также могут вызывать API SDO из языков сценариев, таких как VBScript.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-116">Developers can also call the SDO API from scripting languages such as VBScript.</span></span> <span data-ttu-id="2ed7e-117">Однако так как VBScript ограничен только использованием параметров типа VARIANT, доступна не вся функциональность SDO.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-117">However, because VBScript is limited to using VARIANT-type parameters only, not all the functionality of SDO is available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2ed7e-118">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="2ed7e-118">In This Section</span></span>

[<span data-ttu-id="2ed7e-119">Обзор</span><span class="sxs-lookup"><span data-stu-id="2ed7e-119">Overview</span></span>](/windows/desktop/Nps/sdo-about-server-data-objects)

<span data-ttu-id="2ed7e-120">Общие сведения об API объектов данных сервера.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-120">General information about the Server Data Objects API.</span></span>

[<span data-ttu-id="2ed7e-121">Использующ</span><span class="sxs-lookup"><span data-stu-id="2ed7e-121">Using</span></span>](/windows/desktop/Nps/sdo-using-server-data-objects)

<span data-ttu-id="2ed7e-122">Пример кода, демонстрирующий использование API объектов данных сервера.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-122">Sample code that demonstrates how to use the Server Data Objects API.</span></span>

[<span data-ttu-id="2ed7e-123">Ссылки</span><span class="sxs-lookup"><span data-stu-id="2ed7e-123">Reference</span></span>](/windows/desktop/Nps/sdo-server-data-objects-reference)

<span data-ttu-id="2ed7e-124">Документация по перечисленным типам и интерфейсам, составляющим API объектов данных сервера.</span><span class="sxs-lookup"><span data-stu-id="2ed7e-124">Documentation of the enumerated types and interfaces that compose the Server Data Objects API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ed7e-125">См. также</span><span class="sxs-lookup"><span data-stu-id="2ed7e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed7e-126">Сервер политики сети (служба проверки подлинности в Интернете)</span><span class="sxs-lookup"><span data-stu-id="2ed7e-126">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="2ed7e-127">Служба удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="2ed7e-127">Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 