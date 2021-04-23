---
title: Файлы, созданные для COM-интерфейса
description: Для COM-интерфейсов компилятор MIDL объединяет все вспомогательные подпрограммы и данные клиента и сервера Object Server в единый прокси-файл интерфейса.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- MIDL-компилятор MIDL, MIDL и COM
- COM MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987434"
---
# <a name="files-generated-for-a-com-interface"></a><span data-ttu-id="488c1-105">Файлы, созданные для COM-интерфейса</span><span class="sxs-lookup"><span data-stu-id="488c1-105">Files Generated for a COM Interface</span></span>

<span data-ttu-id="488c1-106">Для COM-интерфейсов компилятор MIDL объединяет все вспомогательные подпрограммы и данные клиента и сервера Object Server в единый прокси-файл интерфейса.</span><span class="sxs-lookup"><span data-stu-id="488c1-106">For COM interfaces, the MIDL compiler combines all client and object server auxiliary routines and data into a single interface proxy file.</span></span> <span data-ttu-id="488c1-107">Этот файл включает суррогатные точки входа как для клиентов, так и для серверов.</span><span class="sxs-lookup"><span data-stu-id="488c1-107">This file includes the surrogate entry points for both clients and servers.</span></span> <span data-ttu-id="488c1-108">Кроме того, компилятор MIDL создает файл заголовка интерфейса, файл UUID интерфейса и файл регистрации интерфейса.</span><span class="sxs-lookup"><span data-stu-id="488c1-108">In addition, the MIDL compiler generates an interface header file, an interface UUID file and an interface registration file.</span></span> <span data-ttu-id="488c1-109">Все эти файлы будут использоваться при создании прокси-библиотеки DLL, содержащей код для поддержки использования интерфейса как клиентскими приложениями, так и серверами объектов.</span><span class="sxs-lookup"><span data-stu-id="488c1-109">You will use all these files when creating a proxy DLL that contains the code to support the use of the interface by both client applications and object servers.</span></span> <span data-ttu-id="488c1-110">При создании исполняемого файла для клиентского приложения, использующего интерфейс, также будет использоваться файл заголовка интерфейса и UUID интерфейса.</span><span class="sxs-lookup"><span data-stu-id="488c1-110">You will also use the interface header file and the interface UUID file when creating the executable file for a client application that uses the interface.</span></span>

<span data-ttu-id="488c1-111">В следующих разделах описываются все файлы, созданные для пользовательского COM-интерфейса, который определяется путем включения **\[** атрибута [**Object**](object.md) **\]** в список атрибутов интерфейса IDL-файла:</span><span class="sxs-lookup"><span data-stu-id="488c1-111">The following topics describe each of the files generated for a custom COM interface, which you identify by including the **\[**[**object**](object.md)**\]** attribute in the interface attribute list of the IDL file:</span></span>

-   [<span data-ttu-id="488c1-112">Прокси-файл интерфейса</span><span class="sxs-lookup"><span data-stu-id="488c1-112">The Interface Proxy File</span></span>](the-interface-proxy-file.md)
-   [<span data-ttu-id="488c1-113">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="488c1-113">The Header Files</span></span>](the-header-files.md)
-   [<span data-ttu-id="488c1-114">Файл UUID интерфейса</span><span class="sxs-lookup"><span data-stu-id="488c1-114">The Interface UUID File</span></span>](the-interface-uuid-file.md)
-   [<span data-ttu-id="488c1-115">Файл регистрации интерфейса</span><span class="sxs-lookup"><span data-stu-id="488c1-115">The Interface Registration File</span></span>](the-interface-registration-file.md)

<span data-ttu-id="488c1-116">Дополнительные сведения см. в статьях [файл конфигурации приложения (ACF)](application-configuration-file-acf-.md), конфигурация [**/АПП \_**](-app-config.md), [файл определения интерфейса (IDL)](interface-definition-idl-file.md), а затем [Сборка и регистрация библиотеки DLL прокси-сервера](../com/building-and-registering-a-proxy-dll.md).</span><span class="sxs-lookup"><span data-stu-id="488c1-116">For more information, see [Application Configuration File (ACF)](application-configuration-file-acf-.md), [**/app\_config**](-app-config.md), [Interface Definition (IDL) File](interface-definition-idl-file.md), and [Building and Registering a Proxy DLL](../com/building-and-registering-a-proxy-dll.md).</span></span>

 

 