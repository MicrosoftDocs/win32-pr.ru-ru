---
title: Совместное использование процедуры ввода-вывода с другими приложениями
description: Совместное использование процедуры ввода-вывода с другими приложениями
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- операции ввода-вывода файлов мультимедиа, общие процедуры
- файловый ввод-вывод, общие процедуры
- входные и выходные данные (ввод-вывод), общие процедуры
- Ввод-вывод (входные и выходные данные), общие процедуры
- Совместное использование процедур ввода-вывода с другими приложениями
- Функция Ммиоинсталлиопрок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412842"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a><span data-ttu-id="ef72c-109">Совместное использование процедуры ввода-вывода с другими приложениями</span><span class="sxs-lookup"><span data-stu-id="ef72c-109">Sharing an I/O Procedure with Other Applications</span></span>

<span data-ttu-id="ef72c-110">Если вы хотите совместно использовать процедуру ввода-вывода с другими приложениями, необходимо написать библиотеку динамической компоновки (DLL) для приложения.</span><span class="sxs-lookup"><span data-stu-id="ef72c-110">If you want to share an I/O procedure with other applications, you need to write a dynamic-link library (DLL) for your application.</span></span> <span data-ttu-id="ef72c-111">Вы можете совместно использовать процедуру ввода-вывода одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="ef72c-111">You can share the I/O procedure by doing one of the following:</span></span>

-   <span data-ttu-id="ef72c-112">Включите код для процедуры ввода-вывода в библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="ef72c-112">Include the code for the I/O procedure in the DLL.</span></span>
-   <span data-ttu-id="ef72c-113">Создайте функцию в библиотеке DLL, которая вызывает функцию [**ммиоинсталлиопрок**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) для установки процедуры ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="ef72c-113">Create a function in the DLL that calls the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function to install the I/O procedure.</span></span>
-   <span data-ttu-id="ef72c-114">Экспортируйте эту функцию в файл определений модуля библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="ef72c-114">Export this function in the module-definitions file of the DLL.</span></span>

<span data-ttu-id="ef72c-115">Чтобы использовать общую процедуру ввода-вывода, приложение должно сначала вызвать функцию в библиотеке DLL, чтобы установить процедуру ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="ef72c-115">To use the shared I/O procedure, an application must first call the function in the DLL to install the I/O procedure.</span></span>

 

 