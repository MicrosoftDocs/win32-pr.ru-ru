---
description: Другим способом создания пространства имен является использование API WMI для программного создания пространства имен.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Создание пространства имен с помощью API инструментария WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711746"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a><span data-ttu-id="65b34-103">Создание пространства имен с помощью API инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="65b34-103">Creating a Namespace with the WMI API</span></span>

<span data-ttu-id="65b34-104">Другим способом создания пространства имен является использование API WMI для программного создания пространства имен.</span><span class="sxs-lookup"><span data-stu-id="65b34-104">Another way of creating a namespace is to use the WMI API to create the namespace programmatically.</span></span> <span data-ttu-id="65b34-105">Преимущество создания пространства имен программным способом заключается в том, что пространство имен можно создать из приложения.</span><span class="sxs-lookup"><span data-stu-id="65b34-105">The advantage to creating a namespace programmatically is that you can create the namespace from within an application.</span></span> <span data-ttu-id="65b34-106">Однако использование API инструментария WMI сложнее, чем использование кода MOF-файл (MOF), и вы не можете легко предоставлять общий доступ к пространствам имен другим разработчикам.</span><span class="sxs-lookup"><span data-stu-id="65b34-106">However, using the WMI API is more complex than using Managed Object Format (MOF) code, and you cannot as easily share your namespaces with other developers.</span></span>

<span data-ttu-id="65b34-107">В следующей процедуре описывается создание пространства имен с помощью API инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="65b34-107">The following procedure describes how to create a namespace using the WMI API.</span></span>

<span data-ttu-id="65b34-108">**Создание пространства имен с помощью API инструментария WMI**</span><span class="sxs-lookup"><span data-stu-id="65b34-108">**To create a namespace using the WMI API**</span></span>

1.  <span data-ttu-id="65b34-109">Используйте [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) для получения указателя на объект [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , указывающий на класс системы [**\_ \_ пространства имен**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="65b34-109">Use [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a pointer to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) object that points to the [**\_\_Namespace**](--namespace.md) system class.</span></span>
2.  <span data-ttu-id="65b34-110">Определите экземпляр класса системы [**\_ \_ пространства имен**](--namespace.md) с помощью вызова [**ивбемклассобжект:: спавнинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span><span class="sxs-lookup"><span data-stu-id="65b34-110">Define an instance of the [**\_\_Namespace**](--namespace.md) system class with a call to [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span></span>
3.  <span data-ttu-id="65b34-111">Задайте свойство **Name** экземпляра [**\_ \_ пространства имен**](--namespace.md) с помощью вызова [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="65b34-111">Set the **Name** property of the [**\_\_Namespace**](--namespace.md) instance with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>
4.  <span data-ttu-id="65b34-112">Создайте пространство имен с помощью вызова [**IWbemServices::P утинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span><span class="sxs-lookup"><span data-stu-id="65b34-112">Create the namespace with a call to [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span></span>

    <span data-ttu-id="65b34-113">Параметр " *закрепление* " [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) должен указывать на новый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="65b34-113">The *pInst* parameter of [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) should point to the new instance.</span></span>

 

 



