---
title: Регистрация работающего сервера EXE
description: Регистрация работающего сервера EXE
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331584"
---
# <a name="registering-a-running-exe-server"></a><span data-ttu-id="8bc36-103">Регистрация работающего сервера EXE</span><span class="sxs-lookup"><span data-stu-id="8bc36-103">Registering a Running EXE Server</span></span>

<span data-ttu-id="8bc36-104">При запуске исполняемого сервера (EXE) он должен вызвать [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), который регистрирует идентификатор CLSID для сервера в том, что называется таблицей класса (другой таблицей, чем у выполняемой таблицы объектов).</span><span class="sxs-lookup"><span data-stu-id="8bc36-104">When an executable (EXE) server is launched, it should call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), which registers the CLSID for the server in what is called the class table (a different table than the running object table).</span></span> <span data-ttu-id="8bc36-105">При регистрации сервера в таблице классов диспетчер управления службами (SCM) может определить, что нет необходимости повторно запускать класс, так как сервер уже запущен.</span><span class="sxs-lookup"><span data-stu-id="8bc36-105">When a server is registered in the class table, it allows the service control manager (SCM) to determine that it is not necessary to launch the class again, because the server is already running.</span></span> <span data-ttu-id="8bc36-106">Если сервер не указан в таблице классов, SCM будет проверять реестр на наличие соответствующих значений и запускать сервер, связанный с данным идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="8bc36-106">Only if the server is not listed in the class table will the SCM check the registry for appropriate values and launch the server associated with the given CLSID.</span></span>

<span data-ttu-id="8bc36-107">Вы передаете [**COREGISTERCLASSOBJECT**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) CLSID для класса и указатель на интерфейс [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8bc36-107">You pass [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) the CLSID for the class and a pointer to its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8bc36-108">Клиенты, которые впоследствии вызывают [**кожетклассобжект**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) с этим идентификатором CLSID, будут получать указатель на запрашиваемый интерфейс, пока безопасность не запрещает ее.</span><span class="sxs-lookup"><span data-stu-id="8bc36-108">Clients who subsequently call [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with this CLSID will retrieve a pointer to their requested interface, as long as security does not forbid it.</span></span> <span data-ttu-id="8bc36-109">(Дополнительные сведения о нескольких функциях создания и активации экземпляров см. в разделе [вспомогательные функции создания экземпляра](instance-creation-helper-functions.md) .)</span><span class="sxs-lookup"><span data-stu-id="8bc36-109">(See [Instance Creation Helper Functions](instance-creation-helper-functions.md) for a description of several instance creation and activation functions.)</span></span>

<span data-ttu-id="8bc36-110">Сервер для объекта класса должен вызвать [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) , чтобы отозвать объект класса (удалить его регистрацию), если выполняются все приведенные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="8bc36-110">The server for a class object should call [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) to revoke the class object (remove its registration) when all of the following are true:</span></span>

-   <span data-ttu-id="8bc36-111">Нет существующих экземпляров определения объекта.</span><span class="sxs-lookup"><span data-stu-id="8bc36-111">There are no existing instances of the object definition.</span></span>
-   <span data-ttu-id="8bc36-112">Нет блокировок для объекта класса.</span><span class="sxs-lookup"><span data-stu-id="8bc36-112">There are no locks on the class object.</span></span>
-   <span data-ttu-id="8bc36-113">Приложение, предоставляющее службы объекту класса, не находится под контролем пользователя (не отображается пользователю на экране).</span><span class="sxs-lookup"><span data-stu-id="8bc36-113">The application providing services to the class object is not under user control (not visible to the user on the display).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bc36-114">См. также</span><span class="sxs-lookup"><span data-stu-id="8bc36-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bc36-115">Установка в качестве приложения службы</span><span class="sxs-lookup"><span data-stu-id="8bc36-115">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="8bc36-116">Регистрация класса при установке</span><span class="sxs-lookup"><span data-stu-id="8bc36-116">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="8bc36-117">Регистрация объектов в таблице ROT</span><span class="sxs-lookup"><span data-stu-id="8bc36-117">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="8bc36-118">Самостоятельная регистрация</span><span class="sxs-lookup"><span data-stu-id="8bc36-118">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 




