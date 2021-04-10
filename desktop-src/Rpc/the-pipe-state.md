---
title: Состояние канала
description: На сервере компилятор MIDL создает переменную состояния, которая координирует процедуры Push, Pull и Alloc.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134179"
---
# <a name="the-pipe-state"></a><span data-ttu-id="f0577-103">Состояние канала</span><span class="sxs-lookup"><span data-stu-id="f0577-103">The Pipe State</span></span>

<span data-ttu-id="f0577-104">На сервере компилятор MIDL создает переменную *состояния* , которая координирует процедуры Push, Pull и Alloc.</span><span class="sxs-lookup"><span data-stu-id="f0577-104">On the server, the MIDL compiler creates a *state* variable that coordinates push, pull, and alloc procedures.</span></span> <span data-ttu-id="f0577-105">На стороне клиента разработчик должен создать переменную *состояния* .</span><span class="sxs-lookup"><span data-stu-id="f0577-105">On the client side, the developer must create the *state* variable.</span></span> <span data-ttu-id="f0577-106">Таким образом, переменная *состояния* является локальной по отношению к обеим сторонам, т. е. Клиент и сервер сохраняют свое собственное состояние канала.</span><span class="sxs-lookup"><span data-stu-id="f0577-106">Therefore, the *state* variable is local to both sides—that is, the client and server each maintain their own pipe state.</span></span> <span data-ttu-id="f0577-107">Код заглушки сервера поддерживает переменную состояния на сервере.</span><span class="sxs-lookup"><span data-stu-id="f0577-107">The server stub code maintains the state variable on the server.</span></span> <span data-ttu-id="f0577-108">Не следует пытаться изменять его содержимое напрямую.</span><span class="sxs-lookup"><span data-stu-id="f0577-108">You should not attempt to modify its contents directly.</span></span> <span data-ttu-id="f0577-109">Клиент должен инициализировать поля в структуре управления канала и поддерживать свою переменную *состояния* .</span><span class="sxs-lookup"><span data-stu-id="f0577-109">The client must initialize the fields in the pipe control structure and maintain its *state* variable.</span></span> <span data-ttu-id="f0577-110">Она использует переменную *состояния* для указания места расположения или размещения данных.</span><span class="sxs-lookup"><span data-stu-id="f0577-110">It uses the *state* variable to identify where to locate or place data.</span></span>

<span data-ttu-id="f0577-111">При передаче данных из одного файла в другой переменная *состояния* клиента может быть такой же простой, как и в случае с файлом.</span><span class="sxs-lookup"><span data-stu-id="f0577-111">The client *state* variable can be as simple as a file handle, if you are transferring data from one file to another.</span></span> <span data-ttu-id="f0577-112">Оно также может быть целым числом, которое указывает на элемент в массиве.</span><span class="sxs-lookup"><span data-stu-id="f0577-112">It can also be an integer that points to an element in an array.</span></span> <span data-ttu-id="f0577-113">Или можно определить довольно сложную структуру состояния для выполнения дополнительных задач, таких как координация push-уведомлений и подпрограммы Pull для параметра \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="f0577-113">Or you can define a fairly complex state structure to perform additional tasks, such as coordinating the push and pull routines on an \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl)\] parameter.</span></span>

 

 