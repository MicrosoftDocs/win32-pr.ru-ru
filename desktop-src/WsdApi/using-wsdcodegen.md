---
description: Описывает процесс создания приложения WSDAPI с помощью Всдкодежен.
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: Использование Всдкодежен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e09bd2b0c8f96d51751aa90bc3206a0824f19b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702285"
---
# <a name="using-wsdcodegen"></a><span data-ttu-id="e06ca-103">Использование Всдкодежен</span><span class="sxs-lookup"><span data-stu-id="e06ca-103">Using WsdCodeGen</span></span>

<span data-ttu-id="e06ca-104">**Создание приложения WSDAPI с помощью Всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="e06ca-104">**To build a WSDAPI application using WsdCodeGen**</span></span>

1.  <span data-ttu-id="e06ca-105">Определите функциональный контракт для узла устройства в WSDL-файле.</span><span class="sxs-lookup"><span data-stu-id="e06ca-105">Define the functional contract for the device host in a WSDL file.</span></span>
2.  <span data-ttu-id="e06ca-106">Создайте файл конфигурации с помощью Всдкодежен.</span><span class="sxs-lookup"><span data-stu-id="e06ca-106">Generate a configuration file using WsdCodeGen.</span></span> <span data-ttu-id="e06ca-107">Дополнительные сведения см. в разделе [файл конфигурации всдкодежен](wsdcodegen-configuration-file.md) и [синтаксис командной строки всдкодежен](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e06ca-107">For more information, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md) and [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
3.  <span data-ttu-id="e06ca-108">Откройте созданный файл конфигурации и при необходимости измените файл.</span><span class="sxs-lookup"><span data-stu-id="e06ca-108">Open the generated configuration file and modify the file as required.</span></span> <span data-ttu-id="e06ca-109">Если вы создаете клиентское приложение, изменение не требуется.</span><span class="sxs-lookup"><span data-stu-id="e06ca-109">If you are building a client application, little or no modification is required.</span></span> <span data-ttu-id="e06ca-110">При создании ведущего приложения измените пользовательские элементы конфигурации (например, [**Manufacturer**](manufacturer.md) и [**modelName**](modelname.md)).</span><span class="sxs-lookup"><span data-stu-id="e06ca-110">If you are building a host application, change the user-specific configuration elements (such as [**manufacturer**](manufacturer.md) and [**modelName**](modelname.md)).</span></span>
4.  <span data-ttu-id="e06ca-111">Создайте код с помощью Всдкодежен, указав файл конфигурации в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="e06ca-111">Generate code using WsdCodeGen, providing the configuration file as input.</span></span> <span data-ttu-id="e06ca-112">Дополнительные сведения см. в описании [синтаксиса командной строки всдкодежен](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e06ca-112">For more information, see [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
5.  <span data-ttu-id="e06ca-113">Используйте созданный код для создания клиента, узла или и того и другого.</span><span class="sxs-lookup"><span data-stu-id="e06ca-113">Use the generated code to build a client, host, or both.</span></span>

<span data-ttu-id="e06ca-114">В Windows SDK содержатся примеры WSDL-файлов, файлы конфигурации Всдкодежен и созданный код.</span><span class="sxs-lookup"><span data-stu-id="e06ca-114">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="e06ca-115">Дополнительные сведения см. в разделе [примеры WSDAPI](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="e06ca-115">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e06ca-116">См. также</span><span class="sxs-lookup"><span data-stu-id="e06ca-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e06ca-117">Примеры WSDAPI</span><span class="sxs-lookup"><span data-stu-id="e06ca-117">WSDAPI Samples</span></span>](wsdapi-samples.md)
</dt> </dl>

 

 



