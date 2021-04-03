---
title: Использование Bluetooth
description: В этом разделе описываются задачи, связанные с написанием приложений на основе Windows для Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797047"
---
# <a name="using-bluetooth"></a><span data-ttu-id="dfc7f-103">Использование Bluetooth</span><span class="sxs-lookup"><span data-stu-id="dfc7f-103">Using Bluetooth</span></span>

<span data-ttu-id="dfc7f-104">В этом разделе описываются задачи, связанные с написанием приложений на основе Windows для Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-104">This section describes tasks that are related to writing Windows-based applications for Bluetooth.</span></span>

<span data-ttu-id="dfc7f-105">Bluetooth предоставляет определения программирования в файлах Ws2bth. h и Блуетусапис. h.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-105">Bluetooth provides programming definitions in the Ws2bth.h and BluetoothAPIs.h files.</span></span> <span data-ttu-id="dfc7f-106">Файл Бссдпдеф. h должен быть добавлен перед Блуетусапис. h.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-106">The Bthsdpdef.h file must be included before BluetoothAPIs.h.</span></span> <span data-ttu-id="dfc7f-107">Файл Ws2bth. h должен быть добавлен после Winsock2. h для использования сокетов Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-107">The Ws2bth.h file must be included after Winsock2.h to use Bluetooth sockets.</span></span> <span data-ttu-id="dfc7f-108">Свяжите только с Бспропс. lib и избегайте связывания с Ирпропс. lib.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-108">Link only to Bthprops.lib, and avoid linking to Irprops.lib.</span></span> <span data-ttu-id="dfc7f-109">Ирпропс. lib предоставляется только для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-109">Irprops.lib is provided for backward compatibility only.</span></span> <span data-ttu-id="dfc7f-110">Бспропс. lib доступен в пакете SDK для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-110">Bthprops.lib is available in the Windows Vista SDK.</span></span> <span data-ttu-id="dfc7f-111">Пакет Windows Vista SDK можно использовать для разработки приложений для Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="dfc7f-111">You can use the Windows Vista SDK to develop applications for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="dfc7f-112">Пакет SDK для Windows Vista доступен в [центре загрузки](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span><span class="sxs-lookup"><span data-stu-id="dfc7f-112">The Windows Vista SDK is available from the [Download Center](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span></span>

<span data-ttu-id="dfc7f-113">Все стандартные синхронные и перекрывающиеся механизмы для чтения и записи данных, которые в настоящее время поддерживаются другими семействами адресов, правильно работают с \_ семейством адресов БС.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-113">All standard synchronous and overlapped mechanisms to read and write data that are currently supported with other address families operate properly with the AF\_BTH address family as well.</span></span>

<span data-ttu-id="dfc7f-114">В пакет SDK входит пример кода, который показывает простое приложение Bluetooth, использующее протоколы Winsock 2,2 и RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-114">There is some example code included with the SDK that shows a simple Bluetooth application using Winsock 2.2 and RFCOMM protocol.</span></span> <span data-ttu-id="dfc7f-115">Исходный код для примера можно найти в расположении установки пакета SDK в разделе C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ <version number> \\ Samples \\ нетдс \\ Winsock \\ Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-115">The source code for the sample can be found in the SDK installation location under C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\winsock\\Bluetooth.</span></span>

<span data-ttu-id="dfc7f-116">В этом разделе описаны следующие темы.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-116">This section describes the following topics.</span></span>



| <span data-ttu-id="dfc7f-117">Section</span><span class="sxs-lookup"><span data-stu-id="dfc7f-117">Section</span></span>                                                                                      | <span data-ttu-id="dfc7f-118">Content</span><span class="sxs-lookup"><span data-stu-id="dfc7f-118">Content</span></span>                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="dfc7f-119">Программирование Bluetooth с помощью сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="dfc7f-119">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md) | <span data-ttu-id="dfc7f-120">Объясняется, как использовать интерфейсы сокетов Windows для реализации сети Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="dfc7f-120">Explains how to use Windows Sockets interfaces to implement a Bluetooth network.</span></span> |



 

 

 




