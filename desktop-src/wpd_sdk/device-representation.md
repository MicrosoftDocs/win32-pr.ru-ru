---
description: Представление устройства
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Представление устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497307"
---
# <a name="device-representation"></a><span data-ttu-id="cc85d-103">Представление устройства</span><span class="sxs-lookup"><span data-stu-id="cc85d-103">Device Representation</span></span>

<span data-ttu-id="cc85d-104">Устройства имеют два основных поведения, которые решаются с помощью архитектуры портативных устройств Windows (WPD):</span><span class="sxs-lookup"><span data-stu-id="cc85d-104">Devices have two main behaviors that are addressed by the Windows Portable Devices (WPD) architecture:</span></span>

-   <span data-ttu-id="cc85d-105">Доступ к содержимому и его хранение.</span><span class="sxs-lookup"><span data-stu-id="cc85d-105">Accessing and storing content.</span></span> <span data-ttu-id="cc85d-106">Например, приложения должны иметь возможность добавлять музыкальные файлы в портативный музыкальный проигрыватель.</span><span class="sxs-lookup"><span data-stu-id="cc85d-106">For example, applications must be able to add music files to a portable music player.</span></span>
-   <span data-ttu-id="cc85d-107">Программирование устройства.</span><span class="sxs-lookup"><span data-stu-id="cc85d-107">Programming the device.</span></span> <span data-ttu-id="cc85d-108">Сюда входят такие простые операции, как изменение параметров и подготовка устройства к сбору данных, или более сложные операции, такие как Загрузка встроенного по.</span><span class="sxs-lookup"><span data-stu-id="cc85d-108">This includes simple operations such as changing settings and preparing the device for data capture, or more complex operations such as uploading firmware.</span></span> <span data-ttu-id="cc85d-109">В качестве примеров можно привести команду "взять фотографию" для цифровой камеры.</span><span class="sxs-lookup"><span data-stu-id="cc85d-109">Examples include issuing a "Take Picture" command to a digital still camera.</span></span>

<span data-ttu-id="cc85d-110">В WPD эти поведения описаны путем представления устройства в виде иерархии объектов.</span><span class="sxs-lookup"><span data-stu-id="cc85d-110">In WPD, these behaviors are described by representing the device as a hierarchy of objects.</span></span> <span data-ttu-id="cc85d-111">На следующем рисунке показано представление объекта WPD для устройства с несколькими функциями, которое в данном случае является мобильным телефоном.</span><span class="sxs-lookup"><span data-stu-id="cc85d-111">The following illustration shows a WPD object representation for a multi-function device, which in this case is a mobile phone.</span></span>

![Иллюстрация, показывающая иерархию объектов для мобильного телефона](images/wpd-overview-figure3.gif)

<span data-ttu-id="cc85d-113">Эта иерархия иллюстрирует следующие функциональные возможности и содержимое.</span><span class="sxs-lookup"><span data-stu-id="cc85d-113">This hierarchy illustrates the following functionality and contents.</span></span>

<span data-ttu-id="cc85d-114">Возможности</span><span class="sxs-lookup"><span data-stu-id="cc85d-114">Functionality:</span></span>

-   <span data-ttu-id="cc85d-115">Объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="cc85d-115">Storage object.</span></span> <span data-ttu-id="cc85d-116">Это устройство имеет хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="cc85d-116">This device has data storage.</span></span>
-   <span data-ttu-id="cc85d-117">Служба контактов.</span><span class="sxs-lookup"><span data-stu-id="cc85d-117">Contacts Service.</span></span> <span data-ttu-id="cc85d-118">Эта служба является функциональным объектом, который можно использовать для синхронизации и хранения контактов на телефоне.</span><span class="sxs-lookup"><span data-stu-id="cc85d-118">This service is a functional object that can be used to synchronize and store contacts on the phone.</span></span>
-   <span data-ttu-id="cc85d-119">Служба SMS.</span><span class="sxs-lookup"><span data-stu-id="cc85d-119">SMS Service.</span></span> <span data-ttu-id="cc85d-120">Эта служба является функциональным объектом, который можно использовать для отправки, получения и хранения SMS-сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc85d-120">This service is a functional object that can be used to send, receive, and store SMS messages.</span></span>

<span data-ttu-id="cc85d-121">Содержимое:</span><span class="sxs-lookup"><span data-stu-id="cc85d-121">Contents:</span></span>

-   <span data-ttu-id="cc85d-122">Объекты мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cc85d-122">Media objects.</span></span> <span data-ttu-id="cc85d-123">Это устройство хранит изображения, музыку и видеофайлы в папках на объекте хранилища.</span><span class="sxs-lookup"><span data-stu-id="cc85d-123">This device stores images, music, and video files in folders on the Storage object.</span></span> <span data-ttu-id="cc85d-124">Хотя файлы, показанные на рисунке, хранятся в одной папке, устройство может разделить содержимое на папки, упорядоченные по типу хранимых носителей. Например, папки изображений, музыкальные папки и видеопапки.</span><span class="sxs-lookup"><span data-stu-id="cc85d-124">While the files shown in the illustration are stored under one folder, a device can subdivide content into folders organized by the type of media stored; for example, image folders, music folders, and video folders.</span></span>
-   <span data-ttu-id="cc85d-125">Объекты Contact.</span><span class="sxs-lookup"><span data-stu-id="cc85d-125">Contact objects.</span></span> <span data-ttu-id="cc85d-126">Это устройство хранит контактные данные (например, имя, номер телефона и адрес) в качестве дочерних элементов службы "Контакты".</span><span class="sxs-lookup"><span data-stu-id="cc85d-126">This device stores contact information (such as name, phone number, and address) as children of the Contacts Service</span></span>
-   <span data-ttu-id="cc85d-127">Объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc85d-127">Message objects.</span></span> <span data-ttu-id="cc85d-128">Это устройство хранит SMS сообщения в виде дочерних элементов службы SMS.</span><span class="sxs-lookup"><span data-stu-id="cc85d-128">This device stores SMS messages as children of the SMS Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc85d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="cc85d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc85d-130">**Общие сведения о приложении**</span><span class="sxs-lookup"><span data-stu-id="cc85d-130">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



