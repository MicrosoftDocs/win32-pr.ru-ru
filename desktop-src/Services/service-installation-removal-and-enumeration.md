---
description: Программа настройки использует функцию CreateService для установки новой службы в базе данных SCM.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Установка, удаление и перечисление служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809443"
---
# <a name="service-installation-removal-and-enumeration"></a><span data-ttu-id="34347-103">Установка, удаление и перечисление служб</span><span class="sxs-lookup"><span data-stu-id="34347-103">Service Installation, Removal, and Enumeration</span></span>

<span data-ttu-id="34347-104">Программа настройки использует функцию [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) для установки новой службы в базе данных SCM.</span><span class="sxs-lookup"><span data-stu-id="34347-104">A configuration program uses the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to install a new service in the SCM database.</span></span> <span data-ttu-id="34347-105">Эта функция задает имя службы и предоставляет сведения о конфигурации, которые хранятся в базе данных.</span><span class="sxs-lookup"><span data-stu-id="34347-105">This function specifies the name of the service and provides configuration information that is stored in the database.</span></span> <span data-ttu-id="34347-106">Описание сведений, хранящихся в базе данных для каждой службы, см. в разделе [Database of Installed Services](database-of-installed-services.md).</span><span class="sxs-lookup"><span data-stu-id="34347-106">For a description of the information stored in the database for each service, see [Database of Installed Services](database-of-installed-services.md).</span></span> <span data-ttu-id="34347-107">Пример кода см. [в разделе Установка службы](installing-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="34347-107">For sample code, see [Installing a Service](installing-a-service.md).</span></span>

<span data-ttu-id="34347-108">Программа настройки использует функцию [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) для удаления установленной службы из базы данных.</span><span class="sxs-lookup"><span data-stu-id="34347-108">A configuration program uses the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to remove an installed service from the database.</span></span> <span data-ttu-id="34347-109">Дополнительные сведения см. [в разделе Удаление службы](deleting-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="34347-109">For more information, see [Deleting a Service](deleting-a-service.md).</span></span>

<span data-ttu-id="34347-110">Чтобы получить имя службы, вызовите функцию [**жетсервицекэйнаме**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) .</span><span class="sxs-lookup"><span data-stu-id="34347-110">To obtain the service name, call the [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) function.</span></span> <span data-ttu-id="34347-111">Отображаемое имя службы, используемое в приложении панели управления "службы", можно получить, вызвав функцию [**жетсервицедисплайнаме**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) .</span><span class="sxs-lookup"><span data-stu-id="34347-111">The service display name, used in the Services control panel applet, can be obtained by calling the [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) function.</span></span>

<span data-ttu-id="34347-112">Программа настройки службы может использовать функцию [**енумсервицесстатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) для перечисления всех служб и их состояний.</span><span class="sxs-lookup"><span data-stu-id="34347-112">A service configuration program can use the [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to enumerate all services and their statuses.</span></span> <span data-ttu-id="34347-113">Кроме того, с помощью функции [**енумдепендентсервицес**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) можно перечислить, какие службы зависят от указанного объекта службы.</span><span class="sxs-lookup"><span data-stu-id="34347-113">It can also use the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate which services are dependent on a specified service object.</span></span>

 

 



