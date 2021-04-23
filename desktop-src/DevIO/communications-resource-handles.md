---
description: Процесс использует функцию CreateFile для открытия маркера для ресурса связи.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Дескрипторы ресурсов связи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423354"
---
# <a name="communications-resource-handles"></a><span data-ttu-id="c6dfd-103">Дескрипторы ресурсов связи</span><span class="sxs-lookup"><span data-stu-id="c6dfd-103">Communications Resource Handles</span></span>

<span data-ttu-id="c6dfd-104">Процесс использует функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) для открытия маркера для ресурса связи.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-104">A process uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a communications resource.</span></span> <span data-ttu-id="c6dfd-105">Например, при указании параметра COM1 открывается маркер для последовательного порта, а порт LPT1 открывает маркер параллельного порта.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-105">For example, specifying COM1 opens a handle to a serial port, and LPT1 opens a handle to a parallel port.</span></span> <span data-ttu-id="c6dfd-106">Если указанный ресурс в настоящее время используется другим процессом, **CreateFile** завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-106">If the specified resource is currently being used by another process, **CreateFile** fails.</span></span> <span data-ttu-id="c6dfd-107">Любой поток процесса может использовать маркер, возвращаемый **CreateFile** , для обнаружения ресурса в любой из функций, обращающихся к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-107">Any thread of the process can use the handle returned by **CreateFile** to identify the resource in any of the functions that access the resource.</span></span>

<span data-ttu-id="c6dfd-108">Когда процесс вызывает [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) для открытия ресурса связи, он задает следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="c6dfd-108">When the process calls [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it specifies the following attributes:</span></span>

-   <span data-ttu-id="c6dfd-109">Какой тип доступа для чтения и записи существует для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-109">What type of read/write access exists for the specified resource.</span></span>
-   <span data-ttu-id="c6dfd-110">Может ли этот маркер наследоваться дочерними процессами.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-110">Whether the handle can be inherited by child processes.</span></span>
-   <span data-ttu-id="c6dfd-111">Может ли этот маркер использоваться в операциях ввода-вывода с перекрытием (асинхронных).</span><span class="sxs-lookup"><span data-stu-id="c6dfd-111">Whether the handle can be used in overlapped (asynchronous) I/O operations.</span></span> <span data-ttu-id="c6dfd-112">(Описание операций с перекрытием см. в разделе [Синхронизация](/windows/desktop/Sync/synchronization).)</span><span class="sxs-lookup"><span data-stu-id="c6dfd-112">(For a description of overlapped operations, see [Synchronization](/windows/desktop/Sync/synchronization).)</span></span>

<span data-ttu-id="c6dfd-113">Когда процесс использует [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) для открытия ресурса связи, он должен указать определенные значения для следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="c6dfd-113">When the process uses [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it must specify certain values for the following parameters:</span></span>

-   <span data-ttu-id="c6dfd-114">Параметр *фдвшаремоде* должен быть равен нулю, что открывает ресурс для монопольного доступа.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-114">The *fdwShareMode* parameter must be zero, opening the resource for exclusive access.</span></span>
-   <span data-ttu-id="c6dfd-115">Параметр *фдвкреате* должен содержать \_ флаг Open existing.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-115">The *fdwCreate* parameter must specify the OPEN\_EXISTING flag.</span></span>
-   <span data-ttu-id="c6dfd-116">Параметр *хтемплатефиле* должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-116">The *hTemplateFile* parameter must be **NULL**.</span></span>

<span data-ttu-id="c6dfd-117">При использовании функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) для открытия обработчика непосредственно на устройстве приложение должно использовать специальные символы " \\ \\ . \\ " для обнаружения устройства.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-117">When using [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a handle directly to a device, an application must use the special characters " \\\\ .\\" to identify the device.</span></span> <span data-ttu-id="c6dfd-118">Например, чтобы открыть обработчик для диска A, укажите \\ \\ . \\ ответ. для параметра *Лпсзнаме* **CreateFile**.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-118">For example, to open a handle to drive A, specify \\\\ .\\a: for the *lpszName* parameter of **CreateFile**.</span></span> <span data-ttu-id="c6dfd-119">Вызывающий процесс может использовать маркер в функции [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) для отправки управляющих кодов на устройство.</span><span class="sxs-lookup"><span data-stu-id="c6dfd-119">The calling process can use the handle in the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function to send control codes to the device.</span></span>

 

 
