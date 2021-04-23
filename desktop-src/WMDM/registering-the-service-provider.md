---
title: Регистрация поставщика услуг
description: Регистрация поставщика услуг
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Диспетчер устройств Windows Media, регистрация поставщиков служб
- Диспетчер устройств, регистрация поставщиков служб
- инструкции по программированию, регистрация поставщиков услуг
- поставщики услуг, регистрация поставщиков услуг
- Создание поставщиков услуг, регистрация поставщиков служб
- Регистрация поставщиков служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067512"
---
# <a name="registering-the-service-provider"></a><span data-ttu-id="4b159-109">Регистрация поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="4b159-109">Registering the Service Provider</span></span>

<span data-ttu-id="4b159-110">Кроме регистрации в качестве COM-объекта, поставщик услуг должен быть зарегистрирован в качестве подключаемого модуля для диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4b159-110">In addition to being registered as a COM object, a service provider must be registered as a plug-in to Windows Media Device Manager.</span></span> <span data-ttu-id="4b159-111">Для регистрации поставщик услуг должен создать следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="4b159-111">To register, a service provider must create the following registry key:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

<span data-ttu-id="4b159-112">В этом разделе < *имя поставщика услуг* > является именем библиотеки DLL. Например, в образце поставщика служб используется Мшдсп.</span><span class="sxs-lookup"><span data-stu-id="4b159-112">In this key, < *your service provider name* > is the name of your DLL; for example, the sample service provider uses MsHDSP.</span></span> <span data-ttu-id="4b159-113">Ключ ProgID должен иметь строковое значение, соответствующее идентификатору CLSID поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="4b159-113">The ProgID key should have a string value that corresponds to the CLSID of your service provider.</span></span> <span data-ttu-id="4b159-114">Например, у примера поставщика служб есть значение «Мдсервицепровидерхд. Мдсервицепровидерхд».</span><span class="sxs-lookup"><span data-stu-id="4b159-114">For instance, the sample service provider has the value "MDServiceProviderHD.MDServiceProviderHD".</span></span>

<span data-ttu-id="4b159-115">Пример реализации DLLRegisterServer поставщика услуг в МДСП. cpp добавляет этот раздел реестра при регистрации образца библиотеки DLL поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="4b159-115">The sample service provider's implementation of DLLRegisterServer in Mdsp.cpp adds this registry key when you register the sample service provider DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b159-116">См. также</span><span class="sxs-lookup"><span data-stu-id="4b159-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b159-117">**Создание поставщика услуг**</span><span class="sxs-lookup"><span data-stu-id="4b159-117">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




