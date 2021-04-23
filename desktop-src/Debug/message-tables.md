---
description: Таблицы сообщений — это специальные строковые ресурсы, используемые при отображении сообщений об ошибках. Они объявляются в файле ресурсов с помощью инструкции МЕССАЖЕТАБЛЕ Resource-Definition. Для доступа к строкам сообщений используйте функцию FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Таблицы сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe12b28c9b4f89d9a6d32c398a2e246940bb79a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990378"
---
# <a name="message-tables"></a><span data-ttu-id="8a678-105">Таблицы сообщений</span><span class="sxs-lookup"><span data-stu-id="8a678-105">Message Tables</span></span>

<span data-ttu-id="8a678-106">Таблицы сообщений — это специальные строковые ресурсы, используемые при отображении сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="8a678-106">Message tables are special string resources used when displaying error messages.</span></span> <span data-ttu-id="8a678-107">Они объявляются в файле ресурсов с помощью инструкции [мессажетабле](../menurc/messagetable-resource.md) Resource-Definition.</span><span class="sxs-lookup"><span data-stu-id="8a678-107">They are declared in a resource file using the [MESSAGETABLE](../menurc/messagetable-resource.md) resource-definition statement.</span></span> <span data-ttu-id="8a678-108">Для доступа к строкам сообщений используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="8a678-108">To access the message strings, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function.</span></span>

<span data-ttu-id="8a678-109">Система предоставляет таблицу сообщений с [кодами системных ошибок](system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8a678-109">The system provides a message table for the [system error codes](system-error-codes.md).</span></span> <span data-ttu-id="8a678-110">Чтобы получить строку, которая соответствует коду ошибки, вызовите метод [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с \_ сообщением Format \_ из \_ системного флага.</span><span class="sxs-lookup"><span data-stu-id="8a678-110">To retrieve the string that corresponds to the error code, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag.</span></span>

<span data-ttu-id="8a678-111">Чтобы предоставить таблицу сообщений для приложения, следуйте инструкциям в [текстовых файлах сообщения](../eventlog/message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="8a678-111">To provide a message table for your application, follow the instructions in [Message Text Files](../eventlog/message-text-files.md).</span></span> <span data-ttu-id="8a678-112">Чтобы получить строки из таблицы сообщений, вызовите метод [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с \_ сообщением Format \_ из \_ флага хмодуле.</span><span class="sxs-lookup"><span data-stu-id="8a678-112">To retrieve strings from your message table, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_HMODULE flag.</span></span>

 

 
