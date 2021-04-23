---
title: Регистрация клиента виртуального канала
description: Необходимо сохранить имя библиотеки DLL клиента в реестре.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792072"
---
# <a name="virtual-channel-client-registration"></a><span data-ttu-id="bcaf2-103">Регистрация клиента виртуального канала</span><span class="sxs-lookup"><span data-stu-id="bcaf2-103">Virtual Channel Client Registration</span></span>

<span data-ttu-id="bcaf2-104">Необходимо сохранить имя библиотеки DLL клиента в реестре.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-104">You must store the name of the client DLL in the registry.</span></span>

<span data-ttu-id="bcaf2-105">В реестре добавьте подраздел в одно из следующих расположений:</span><span class="sxs-lookup"><span data-stu-id="bcaf2-105">In the registry, add a subkey to one of the following locations:</span></span>

<span data-ttu-id="bcaf2-106">**HKey \_ Текущие \_ пользовательские** \\ **программные** \\  \\  \\  \\ **надстройки** клиента сервера терминалов Microsoft</span><span class="sxs-lookup"><span data-stu-id="bcaf2-106">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**Addins**</span></span>

<span data-ttu-id="bcaf2-107">**HKey \_ Текущая \_ Пользовательская** \\ **Программа**. \\  \\  \\  \\ **надстройки** для подключения клиента сервера терминалов Microsoft</span><span class="sxs-lookup"><span data-stu-id="bcaf2-107">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**connection**\\**Addins**</span></span>

> [!Note]  
> <span data-ttu-id="bcaf2-108">В пути реестра *Connection* представляет имя соединения в диспетчере соединений.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-108">In the registry path, *connection* represents the name of a connection in Connection Manager.</span></span>

 

<span data-ttu-id="bcaf2-109">Записи в разделе **\\ \\ ADDIN по умолчанию** применяются ко всем подключениям.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-109">Entries under the **\\Default\\Addins** key apply to all connections.</span></span> <span data-ttu-id="bcaf2-110">Записи в разделе " **\\  \\ надстройки подключений** " применяются только к соединению, определяемому *соединением*.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-110">Entries under the **\\***connection***\\Addins** key apply only to the connection identified by *connection*.</span></span> <span data-ttu-id="bcaf2-111">Подключения могут создаваться и управляться с помощью диспетчера соединений.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-111">Connections can be created and managed by using Connection Manager.</span></span>

<span data-ttu-id="bcaf2-112">Подразделу можно присвоить любое имя.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-112">The subkey can be given any name.</span></span> <span data-ttu-id="bcaf2-113">Он должен содержать значение **reg \_ SZ** или **reg \_ expand \_ SZ** , а также может содержать значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="bcaf2-113">It must contain a **REG\_SZ** or **REG\_EXPAND\_SZ** value and may optionally contain a **REG\_DWORD** value.</span></span> <span data-ttu-id="bcaf2-114">Синтаксис значения **reg \_ SZ** или **reg \_ expand \_ SZ** выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-114">The syntax of the **REG\_SZ** or **REG\_EXPAND\_SZ** value is as follows.</span></span>

``` syntax
Name = DLLname
```

<span data-ttu-id="bcaf2-115">Если **Name** — это **значение \_ \_ SZ Expand** , оно может содержать неразвернутые переменные среды, которые расширяются во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-115">If **Name** is a **REG\_EXPAND\_SZ** value, it can contain unexpanded environment variables that are expanded at runtime.</span></span>

<span data-ttu-id="bcaf2-116">Значением *DLLname* может быть полный путь.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-116">The value of *DLLname* can be a fully qualified path.</span></span> <span data-ttu-id="bcaf2-117">Если параметр *DLLname* не содержит путь, используется стандартная стратегия поиска DLL.</span><span class="sxs-lookup"><span data-stu-id="bcaf2-117">If *DLLname* does not contain a path, the standard DLL search strategy is used.</span></span> <span data-ttu-id="bcaf2-118">Дополнительные сведения см. в разделе "Примечания" для [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="bcaf2-118">For more information, see the Remarks section for [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

 

 