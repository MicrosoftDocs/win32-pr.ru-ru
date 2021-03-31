---
description: Управление доступом
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Управление доступом (API-интерфейс WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912891"
---
# <a name="access-control-wpd-api"></a><span data-ttu-id="cc365-103">Управление доступом (API-интерфейс WPD)</span><span class="sxs-lookup"><span data-stu-id="cc365-103">Access Control (WPD API)</span></span>

<span data-ttu-id="cc365-104">WDM (WDM) поддерживает запрещение доступа к устройствам через списки управления доступом (ACL) на узлах устройств самонастраивающийся (PnP).</span><span class="sxs-lookup"><span data-stu-id="cc365-104">The Windows Driver Model (WDM) supports restricting device access via Access Control Lists (ACLs) on the Plug and Play (PnP) Device Nodes.</span></span> <span data-ttu-id="cc365-105">Это означает, что поставщики и сетевые администраторы могут ограничить доступ к любому типу устройства.</span><span class="sxs-lookup"><span data-stu-id="cc365-105">This means that vendors and network administrators can restrict access to any device type.</span></span> <span data-ttu-id="cc365-106">Когда приложение открывает обработчик для драйвера с помощью вызова [**ипортабледевице:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), диспетчер ввода-вывода драйвера проверяет, имеет ли данный пользователь необходимый доступ, и аналогично проверяет, когда ioctl отправляются драйверу из этого обработчика.</span><span class="sxs-lookup"><span data-stu-id="cc365-106">When an application opens a handle to a driver by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), the driver's I/O Manager verifies whether the given user has the required access, and similarly does access checks when IOCTLs are sent to the driver from that handle.</span></span>

<span data-ttu-id="cc365-107">Например, администратор сети может ограничить гостевые пользователи доступом только для чтения для портативных устройств, в то время как они могут предоставить пользователям, прошедшим проверку подлинности, доступ на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="cc365-107">For example, a network administrator could restrict Guest users to read-only access for portable devices, while they could grant Authenticated users read/write access.</span></span> <span data-ttu-id="cc365-108">В этом случае это означает, что если гостевая виртуальная машина выдала команду WPD, которая требует доступа на чтение и запись (например, удаление объекта); в этом случае произойдет отказ в доступе, тогда как если пользователь, прошедший проверку подлинности, выпустил ту же команду, он будет успешным.</span><span class="sxs-lookup"><span data-stu-id="cc365-108">In this case, it implies that if a Guest issued a WPD command that required read/write access (such as Delete Object); it would fail with Access Denied, whereas if an Authenticated user issued the same command, it would succeed.</span></span>

<span data-ttu-id="cc365-109">Записи групповая политика для управления доступом к съемным и портативным устройствам на самом деле не являются простым способом для администраторов применять списки ACL узла устройства PnP к целому классу устройств за раз (например, при применении параметра "запретить доступ на запись для портативных устройств" групповая политика списки ACL для всех устройств типа WPD, чтобы запретить доступ на запись).</span><span class="sxs-lookup"><span data-stu-id="cc365-109">The Group Policy entries for controlling access to removable storage and portable devices is actually nothing more than an easy way for Administrators to apply PnP device node ACLs to a whole class of devices at a time (for example, applying the "Deny Write Access to Portable Devices" Group Policy would adjust the ACLs of all WPD devices to deny write access).</span></span>

## <a name="io-control-codes-in-wpd"></a><span data-ttu-id="cc365-110">Управляющие коды ввода-вывода в WPD</span><span class="sxs-lookup"><span data-stu-id="cc365-110">I/O Control Codes in WPD</span></span>

<span data-ttu-id="cc365-111">Приложения WPD взаимодействуют с драйверами, открывая дескрипторы устройств и отправляя управляющие коды ввода-вывода (IOCTL).</span><span class="sxs-lookup"><span data-stu-id="cc365-111">WPD applications communicate with drivers by opening device handles and sending I/O Control Codes (IOCTLs).</span></span> <span data-ttu-id="cc365-112">Эти IOCTL состоят из четырех разделов:</span><span class="sxs-lookup"><span data-stu-id="cc365-112">These IOCTLs consist of four sections:</span></span>

1.  <span data-ttu-id="cc365-113">Тип устройства</span><span class="sxs-lookup"><span data-stu-id="cc365-113">Device Type</span></span>
2.  <span data-ttu-id="cc365-114">Код функции</span><span class="sxs-lookup"><span data-stu-id="cc365-114">Function Code</span></span>
3.  <span data-ttu-id="cc365-115">Buffer, метод</span><span class="sxs-lookup"><span data-stu-id="cc365-115">Buffer Method</span></span>
4.  <span data-ttu-id="cc365-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="cc365-116">Access Type</span></span>

<span data-ttu-id="cc365-117">Четвертый раздел, тип доступа, задает конкретные требования к доступу для заданной команды.</span><span class="sxs-lookup"><span data-stu-id="cc365-117">The fourth section, the Access Type, specifies the specific access requirement for the given command.</span></span> <span data-ttu-id="cc365-118">Диспетчер ввода-вывода драйвера использует эти данные для выполнения проверки списка управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="cc365-118">The driver's I/O manager uses this data to perform the Access Control List (ACL) check.</span></span>

<span data-ttu-id="cc365-119">Поэтому, если запрос IOCTL был определен как:</span><span class="sxs-lookup"><span data-stu-id="cc365-119">So if an IOCTL were defined as:</span></span>


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



<span data-ttu-id="cc365-120">Диспетчер ввода-вывода драйвера проверяет, имеет ли владелец маркера устройства доступ на чтение к устройству при отправке этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="cc365-120">The driver's I/O manager would check that the owner of the device handle has read access to the device when this message is sent.</span></span>

<span data-ttu-id="cc365-121">И, если запрос IOCTL был определен как:</span><span class="sxs-lookup"><span data-stu-id="cc365-121">And, if an IOCTL were defined as:</span></span>


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



<span data-ttu-id="cc365-122">Диспетчер ввода-вывода драйвера проверяет, имеет ли владелец маркера устройства доступ на чтение и запись к устройству при отправке этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="cc365-122">The driver's I/O manager would check that the owner of the device handle has read/write access to the device when this message is sent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc365-123">См. также</span><span class="sxs-lookup"><span data-stu-id="cc365-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc365-124">**Общие сведения о приложении**</span><span class="sxs-lookup"><span data-stu-id="cc365-124">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="cc365-125">**Ипортабледевице:: Open**</span><span class="sxs-lookup"><span data-stu-id="cc365-125">**IPortableDevice::Open**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[<span data-ttu-id="cc365-126">**Ипортабледевице:: Сендкомманд**</span><span class="sxs-lookup"><span data-stu-id="cc365-126">**IPortableDevice::SendCommand**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



