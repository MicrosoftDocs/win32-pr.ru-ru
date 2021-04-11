---
description: Команды
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Команды (API-интерфейс WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263021"
---
# <a name="commands-wpd-api"></a><span data-ttu-id="3cff9-103">Команды (API-интерфейс WPD)</span><span class="sxs-lookup"><span data-stu-id="3cff9-103">Commands (WPD API)</span></span>

<span data-ttu-id="3cff9-104">Клиентское приложение и драйвер взаимодействуют с помощью команд, отправленных с клиента (через API переносных устройств Windows) в драйвер (через платформу драйверов User-Mode).</span><span class="sxs-lookup"><span data-stu-id="3cff9-104">The client application and the driver communicate by means of commands that are sent from the client (via the Windows Portable Device API) to the driver (via the User-Mode Driver Framework).</span></span> <span data-ttu-id="3cff9-105">Команда может содержать или не включать параметр, а также не может возвращать результат.</span><span class="sxs-lookup"><span data-stu-id="3cff9-105">A command may or may not include a parameter, and may or may not return a result.</span></span> <span data-ttu-id="3cff9-106">Клиент может явно отправить команду, вызвав метод [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) или **ипортабледевицесервице: сендкомманд** или неявно, вызвав любой из методов клиентского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3cff9-106">A client can send a command explicitly, by calling either the [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) method or the **IPortableDeviceService:SendCommand** method, or implicitly, by calling any of the methods of the client interfaces.</span></span> <span data-ttu-id="3cff9-107">Несколько команд можно отправить только явным образом. они указаны в документации по команде.</span><span class="sxs-lookup"><span data-stu-id="3cff9-107">A few commands can only be sent explicitly; these are noted in the command's documentation.</span></span> <span data-ttu-id="3cff9-108">На страницах справочника по командам описывается назначение команды, а также параметры, которые она ожидает получить, и параметры, которые она должна возвращать.</span><span class="sxs-lookup"><span data-stu-id="3cff9-108">The command reference pages describe the purpose of a command, as well as what parameters it expects to receive, and what parameters it is expected to return.</span></span>

<span data-ttu-id="3cff9-109">Команда определяется структурой **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="3cff9-109">A command is identified by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="3cff9-110">Это состоит из двух частей: части идентификатора GUID (элемент *fmtid* ) и части DWORD (элемент *PID* ).</span><span class="sxs-lookup"><span data-stu-id="3cff9-110">This is made up of two parts: a GUID part (the *fmtid* member) and a DWORD part (the *pid* member).</span></span> <span data-ttu-id="3cff9-111">Часть идентификатора GUID используется для указания категории, которой принадлежит команда (связанные команды относятся к той же категории и, следовательно, будут иметь тот же *fmtid*).</span><span class="sxs-lookup"><span data-stu-id="3cff9-111">The GUID part is used to indicate the category the command belongs to (related commands belong to the same category, and therefore will have the same *fmtid*).</span></span> <span data-ttu-id="3cff9-112">Часть DWORD указывает идентификатор команды и используется для различения отдельных команд в категории команд (значения *PID* для команд в той же категории будут отличаться).</span><span class="sxs-lookup"><span data-stu-id="3cff9-112">The DWORD part indicates the command ID, and is used to distinguish the individual commands within a command category (the *pid* values for commands in the same category will be different).</span></span>

<span data-ttu-id="3cff9-113">В следующей таблице перечислены категории команд, определяемых портативными устройствами Windows.</span><span class="sxs-lookup"><span data-stu-id="3cff9-113">The following table lists the categories of commands that Windows Portable Devices defines.</span></span> <span data-ttu-id="3cff9-114">Производители устройств могут определять собственные команды, создавая собственные категории команд и идентификаторы команд.</span><span class="sxs-lookup"><span data-stu-id="3cff9-114">Device manufacturers can define their own commands by creating their own command categories and command IDs.</span></span> <span data-ttu-id="3cff9-115">Однако изготовителю не следует добавлять команды в указанные ниже категории, так как они зарезервированы корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3cff9-115">However, a manufacturer should not add commands to the categories listed below, since these are reserved by Microsoft.</span></span>

<span data-ttu-id="3cff9-116">**Категории команд**</span><span class="sxs-lookup"><span data-stu-id="3cff9-116">**Command Categories**</span></span>



| <span data-ttu-id="3cff9-117">Категория команды</span><span class="sxs-lookup"><span data-stu-id="3cff9-117">Command category</span></span>                         | <span data-ttu-id="3cff9-118">Описание</span><span class="sxs-lookup"><span data-stu-id="3cff9-118">Description</span></span>                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cff9-119">**\_Категория WPD \_ Common**</span><span class="sxs-lookup"><span data-stu-id="3cff9-119">**WPD\_CATEGORY\_COMMON**</span></span>                | <span data-ttu-id="3cff9-120">Команды, общие для всех объектов и устройств.</span><span class="sxs-lookup"><span data-stu-id="3cff9-120">Commands that are common to all objects and devices.</span></span>                                                                                    |
| <span data-ttu-id="3cff9-121">**\_указания для \_ устройств \_ категории WPD**</span><span class="sxs-lookup"><span data-stu-id="3cff9-121">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>         | <span data-ttu-id="3cff9-122">Команды, используемые для получения дополнительных сведений об устройстве, которые можно использовать для улучшения взаимодействия с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="3cff9-122">Commands that are used to retrieve optional device information that can be used to improve end-user experience.</span></span>                         |
| <span data-ttu-id="3cff9-123">**\_Категория WPD \_ SMS**</span><span class="sxs-lookup"><span data-stu-id="3cff9-123">**WPD\_CATEGORY\_SMS**</span></span>                   | <span data-ttu-id="3cff9-124">Команды, используемые для устройств с поддержкой функций SMS, которые обычно предоставляются на мобильных телефонах.</span><span class="sxs-lookup"><span data-stu-id="3cff9-124">Commands that are used for devices that support short message service (SMS) functionality, which is typically exposed on mobile phones.</span></span> |
| <span data-ttu-id="3cff9-125">**\_Категория WPD \_ все \_ еще \_ отслеживает образы**</span><span class="sxs-lookup"><span data-stu-id="3cff9-125">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span> | <span data-ttu-id="3cff9-126">Команды, используемые для устройств, которые поддерживают запись образов.</span><span class="sxs-lookup"><span data-stu-id="3cff9-126">Commands that are used for devices that support still image capture.</span></span>                                                                    |
| <span data-ttu-id="3cff9-127">**\_хранилище категорий \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="3cff9-127">**WPD\_CATEGORY\_STORAGE**</span></span>               | <span data-ttu-id="3cff9-128">Команды, используемые для функциональных объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="3cff9-128">Commands that are used for storage functional objects.</span></span>                                                                                  |



 

<span data-ttu-id="3cff9-129">Конкретные команды, определенные для каждого из этих типов, приведены в следующих таблицах, упорядоченных по типу команды.</span><span class="sxs-lookup"><span data-stu-id="3cff9-129">The specific commands that are defined for each of these types are given in the following tables, organized by command type.</span></span>

<span data-ttu-id="3cff9-130">**\_ \_ Общая категория категории WPD**</span><span class="sxs-lookup"><span data-stu-id="3cff9-130">**WPD\_CATEGORY\_COMMON Category**</span></span>



| <span data-ttu-id="3cff9-131">Get-Help</span><span class="sxs-lookup"><span data-stu-id="3cff9-131">Command</span></span>                                                                                | <span data-ttu-id="3cff9-132">Описание</span><span class="sxs-lookup"><span data-stu-id="3cff9-132">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="3cff9-133">**\_устройство с \_ общим \_ СБРОСом команды \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="3cff9-133">**WPD\_COMMAND\_COMMON\_RESET\_DEVICE**</span></span>](wpd-command-common-reset-device-command.md) | <span data-ttu-id="3cff9-134">Выполняет сброс устройства.</span><span class="sxs-lookup"><span data-stu-id="3cff9-134">Resets the device.</span></span> |



 

<span data-ttu-id="3cff9-135">**Категория WPD категории \_ \_ \_ подсказок устройства**</span><span class="sxs-lookup"><span data-stu-id="3cff9-135">**WPD\_CATEGORY\_DEVICE\_HINTS Category**</span></span>



| <span data-ttu-id="3cff9-136">Get-Help</span><span class="sxs-lookup"><span data-stu-id="3cff9-136">Command</span></span>                                                                                                              | <span data-ttu-id="3cff9-137">Описание</span><span class="sxs-lookup"><span data-stu-id="3cff9-137">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="3cff9-138">**\_устройства с командными \_ \_ указаниями WPD \_ Получение \_ \_ расположения содержимого**</span><span class="sxs-lookup"><span data-stu-id="3cff9-138">**WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION**</span></span>](wpd-command-device-hints-get-content-location-command.md) | <span data-ttu-id="3cff9-139">Извлекает идентификаторы объектов папок, которые могут содержать объект указанного типа.</span><span class="sxs-lookup"><span data-stu-id="3cff9-139">Retrieves the object IDs of folders that can hold an object of a specified type.</span></span> |



 

<span data-ttu-id="3cff9-140">**\_ \_ Категория хранилища категории WPD**</span><span class="sxs-lookup"><span data-stu-id="3cff9-140">**WPD\_CATEGORY\_STORAGE Category**</span></span>



| <span data-ttu-id="3cff9-141">Get-Help</span><span class="sxs-lookup"><span data-stu-id="3cff9-141">Command</span></span>                                                                     | <span data-ttu-id="3cff9-142">Описание</span><span class="sxs-lookup"><span data-stu-id="3cff9-142">Description</span></span>                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="3cff9-143">**\_ \_ Извлечение хранилища команд \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="3cff9-143">**WPD\_COMMAND\_STORAGE\_EJECT**</span></span>](wpd-command-storage-eject-command.md)   | <span data-ttu-id="3cff9-144">Извлекает носитель, который можно удаленно извлечь с помощью драйвера.</span><span class="sxs-lookup"><span data-stu-id="3cff9-144">Ejects a storage medium that can be ejected remotely by the driver.</span></span> |
| [<span data-ttu-id="3cff9-145">**\_ \_ Формат хранилища команд \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="3cff9-145">**WPD\_COMMAND\_STORAGE\_FORMAT**</span></span>](wpd-command-storage-format-command.md) | <span data-ttu-id="3cff9-146">Форматирует функциональный объект хранилища на устройстве.</span><span class="sxs-lookup"><span data-stu-id="3cff9-146">Formats a storage functional object on the device.</span></span>                  |



 

<span data-ttu-id="3cff9-147">**Категория "WPD" категории " \_ \_ SMS"**</span><span class="sxs-lookup"><span data-stu-id="3cff9-147">**WPD\_CATEGORY\_SMS Category**</span></span>



| <span data-ttu-id="3cff9-148">Get-Help</span><span class="sxs-lookup"><span data-stu-id="3cff9-148">Command</span></span>                                                         | <span data-ttu-id="3cff9-149">Описание</span><span class="sxs-lookup"><span data-stu-id="3cff9-149">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="3cff9-150">**\_команда WPD \_ , \_ Отправка SMS**</span><span class="sxs-lookup"><span data-stu-id="3cff9-150">**WPD\_COMMAND\_SMS\_SEND**</span></span>](wpd-command-sms-send-command.md) | <span data-ttu-id="3cff9-151">Инициирует отправку сообщения SMS функциональным объектом SMS.</span><span class="sxs-lookup"><span data-stu-id="3cff9-151">Initiates the sending of an SMS message by an SMS functional object.</span></span> |



 

<span data-ttu-id="3cff9-152">**Категория "WPD" \_ \_ все еще имеет \_ \_ категорию захвата образа**</span><span class="sxs-lookup"><span data-stu-id="3cff9-152">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE Category**</span></span>



| <span data-ttu-id="3cff9-153">Get-Help</span><span class="sxs-lookup"><span data-stu-id="3cff9-153">Command</span></span>                                                                                                   | <span data-ttu-id="3cff9-154">Описание</span><span class="sxs-lookup"><span data-stu-id="3cff9-154">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="3cff9-155">**\_команда WPD \_ все \_ еще \_ запускает запись образа \_**</span><span class="sxs-lookup"><span data-stu-id="3cff9-155">**WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE**</span></span>](wpd-command-still-image-capture-initiate-command.md) | <span data-ttu-id="3cff9-156">Инициирует запись образа по-прежнему с помощью функционального объекта Image.</span><span class="sxs-lookup"><span data-stu-id="3cff9-156">Initiates a still image capture by a still image functional object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3cff9-157">См. также</span><span class="sxs-lookup"><span data-stu-id="3cff9-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cff9-158">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="3cff9-158">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



