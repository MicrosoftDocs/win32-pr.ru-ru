---
title: Файл регистрации интерфейса
description: Файл регистрации интерфейса собирает сведения, которые помогают в регистрации интерфейсов COM, упакованных в DLL-файл или в ИСПОЛНЯЕМые файлы.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- файл регистрации интерфейса MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd6f54f5e027a0ea25dc463772ec24ee5f7386
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661719"
---
# <a name="the-interface-registration-file"></a><span data-ttu-id="fde0b-104">Файл регистрации интерфейса</span><span class="sxs-lookup"><span data-stu-id="fde0b-104">The Interface Registration File</span></span>

<span data-ttu-id="fde0b-105">Файл регистрации интерфейса собирает сведения, которые помогают в регистрации интерфейсов COM, упакованных в DLL-файл или в ИСПОЛНЯЕМые файлы.</span><span class="sxs-lookup"><span data-stu-id="fde0b-105">The interface registration file collects information that helps in the registration of COM interfaces packaged into a DLL or EXE file.</span></span> <span data-ttu-id="fde0b-106">Файл регистрации интерфейса отличается от других созданных файлов, так как он может собирать информацию из нескольких разных IDL-файлов.</span><span class="sxs-lookup"><span data-stu-id="fde0b-106">The interface registration file is different from other generated files because it can gather information from compiling several different IDL files.</span></span> <span data-ttu-id="fde0b-107">Каждый запуск компилятора MIDL для COM-интерфейсов ищет существующий файл DLLDATA. c, а если файл не найден, создается новый файл DLLDATA. c.</span><span class="sxs-lookup"><span data-stu-id="fde0b-107">Each MIDL compiler run for COM interfaces looks for an existing dlldata.c file first, and if the file is not found, a new dlldata.c file is created.</span></span> <span data-ttu-id="fde0b-108">При обнаружении файла DLLDATA. c сведения о текущем IDL-файле добавляются (если они отсутствуют) или заменяются.</span><span class="sxs-lookup"><span data-stu-id="fde0b-108">If a dlldata.c file is found, information about the current IDL is added (if absent) or replaced.</span></span>

<span data-ttu-id="fde0b-109">Файл регистрации интерфейса безопасно создается или обновляется в многопроцессорной среде, так как параллельные компиляции MIDL не могут одновременно выполнять запись в файл.</span><span class="sxs-lookup"><span data-stu-id="fde0b-109">The interface registration file is safely generated or updated in a multiprocessor environment because parallel MIDL compiles are prevented from writing to the file at the same time.</span></span> <span data-ttu-id="fde0b-110">Поскольку любой файл DLLDATA. c может быть помечен только для чтения средой сборки или пользователем, компилятор MIDL реализует метод timeout для ожидания файла, который он не может открыть, и выдает соответствующее сообщение об ошибке по истечении времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="fde0b-110">Because any dlldata.c file can be marked as read-only by either the build environment or the user, the MIDL compiler implements a timeout approach to waiting on a file it cannot open, and issues an appropriate error message if the timeout expires.</span></span>

<span data-ttu-id="fde0b-111">Имя по умолчанию для файла регистрации интерфейса, созданного из входного файла, — DLLDATA. c.</span><span class="sxs-lookup"><span data-stu-id="fde0b-111">The default name for the interface registration file generated from an input file is dlldata.c.</span></span> <span data-ttu-id="fde0b-112">Параметр компилятора [**/dlldata**](-dlldata.md) MIDL можно использовать для переопределения имени файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fde0b-112">The [**/dlldata**](-dlldata.md) MIDL compiler switch can be used to override the default name of the file.</span></span> <span data-ttu-id="fde0b-113">Переопределение имени файла регистрации интерфейса по умолчанию особенно полезно, когда некоторые файлы IDL, Упакованные в общий двоичный файл, находятся в разных каталогах.</span><span class="sxs-lookup"><span data-stu-id="fde0b-113">Overriding the default name of the interface registration file is especially useful when some IDL files packaged to a common binary reside in different directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fde0b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="fde0b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fde0b-115">Создание и регистрация библиотеки DLL прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="fde0b-115">Building and Registering a Proxy DLL</span></span>](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 