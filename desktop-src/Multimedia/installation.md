---
title: Установка (мультимедиа Windows)
description: Установка
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- устанавливаемые драйверы, установка
- устанавливаемые драйверы, DRV_INSTALL сообщение
- устанавливаемые драйверы, DRV_REMOVE сообщение
- Сообщение DRV_INSTALL
- Сообщение DRV_REMOVE
- Сообщение ДРВКОНФИГИНФО
- Установка драйверов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ebebd090c7499698c59c325d1ac0d487902454
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414508"
---
# <a name="installation-windows-multimedia"></a><span data-ttu-id="a4c77-110">Установка (мультимедиа Windows)</span><span class="sxs-lookup"><span data-stu-id="a4c77-110">Installation (Windows Multimedia)</span></span>

<span data-ttu-id="a4c77-111">Устанавливаемый драйвер может выполнять задачи установки, относящиеся к драйверу, при обработке сообщений об [**\_ удалении**](drv-remove.md) [**и копии DRV. \_**](drv-install.md)</span><span class="sxs-lookup"><span data-stu-id="a4c77-111">An installable driver can carry out driver-specific installation tasks when processing the [**DRV\_INSTALL**](drv-install.md) and [**DRV\_REMOVE**](drv-remove.md) messages.</span></span> <span data-ttu-id="a4c77-112">Приложение установки, например приложение панели управления, отправляет сообщения драйверу при установке или удалении драйвера соответственно.</span><span class="sxs-lookup"><span data-stu-id="a4c77-112">An installation application, such as a Control Panel application, sends the messages to the driver when installing or removing the driver, respectively.</span></span>

<span data-ttu-id="a4c77-113">При обработке \_ сообщения об установке DRV драйвер обычно проверяет наличие необходимого оборудования, а затем отображает диалоговое окно Конфигурация, позволяющее пользователю выбрать начальные параметры конфигурации для драйвера и связанного с ним оборудования.</span><span class="sxs-lookup"><span data-stu-id="a4c77-113">When processing the DRV\_INSTALL message, the driver typically verifies that the required hardware is present and then displays the configuration dialog box to let the user choose the initial configuration settings for the driver and associated hardware.</span></span> <span data-ttu-id="a4c77-114">Сообщение содержит адрес структуры [**дрвконфигинфо**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) , содержащей имена раздела реестра и значения, связанные с драйвером. драйвер проверяет значение реестра для сведений о конфигурации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4c77-114">The message includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver; the driver checks the registry value for default configuration information.</span></span> <span data-ttu-id="a4c77-115">Наконец, драйвер также создает дополнительные разделы реестра и значения, необходимые для успешной работы.</span><span class="sxs-lookup"><span data-stu-id="a4c77-115">Finally, the driver also creates any additional registry keys and values needed for successful operation.</span></span>

<span data-ttu-id="a4c77-116">При обработке \_ сообщения об удалении DRV драйвер удаляет все разделы реестра и значения, которые могли быть созданы.</span><span class="sxs-lookup"><span data-stu-id="a4c77-116">When processing the DRV\_REMOVE message, the driver removes any registry keys and values it may have created.</span></span>

 

 
