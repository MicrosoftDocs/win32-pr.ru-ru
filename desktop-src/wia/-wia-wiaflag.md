---
description: 'Флаги, используемые методами Ивиадевмгр:: Жетимажедлг, IWiaDevMgr2:: Жетимажедлг, Ивиаитем::D Евицедлг и IWiaItem2::D Евицедлг для управления операцией диалогового окна.'
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: Виафлаг (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c906f22e168ca29aadd2e9450fac6225c8b91c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656119"
---
# <a name="wiaflag"></a><span data-ttu-id="e03d6-103">виафлаг</span><span class="sxs-lookup"><span data-stu-id="e03d6-103">WiaFlag</span></span>

<span data-ttu-id="e03d6-104">Флаги, используемые методами [**ивиадевмгр:: жетимажедлг**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2:: жетимажедлг**](-wia-iwiadevmgr2-getimagedlg.md), [**Ивиаитем::D Евицедлг**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)и [**IWiaItem2::D евицедлг**](-wia-iwiaitem2-devicedlg.md) для управления операцией диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="e03d6-104">Flags used by the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg), and [**IWiaItem2::DeviceDlg**](-wia-iwiaitem2-devicedlg.md) methods to control the dialog box operation.</span></span>



| <span data-ttu-id="e03d6-105">Константа</span><span class="sxs-lookup"><span data-stu-id="e03d6-105">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="e03d6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e03d6-106">Description</span></span>                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <span data-ttu-id="e03d6-107"><dt>**\_ \_ \_ одиночное изображение диалогового окна WIA устройства \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e03d6-107"><dt>**WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE**</dt></span></span> </dl>     | <span data-ttu-id="e03d6-108">Ограничить выбор изображения одним изображением в диалоговом окне "получение образа устройства".</span><span class="sxs-lookup"><span data-stu-id="e03d6-108">Restrict image selection to a single image in the device image acquisition dialog box.</span></span><br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <span data-ttu-id="e03d6-109"><dt>**\_ \_ \_ \_ Общий \_ Пользовательский интерфейс диалогового окна устройства WIA**</dt></span><span class="sxs-lookup"><span data-stu-id="e03d6-109"><dt>**WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI**</dt></span></span> </dl> | <span data-ttu-id="e03d6-110">Используйте пользовательский интерфейс системы, если он доступен, а не пользовательский интерфейс, предоставляемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="e03d6-110">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="e03d6-111">Если пользовательский интерфейс системы недоступен, используется пользовательский интерфейс поставщика.</span><span class="sxs-lookup"><span data-stu-id="e03d6-111">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="e03d6-112">Если ни один из ИНТЕРФЕЙСов не доступен, функция возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="e03d6-112">If neither UI is available, the function returns E\_NOTIMPL.</span></span><br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <span data-ttu-id="e03d6-113"><dt>**WIA \_ SELECT \_ устройство не \_ по умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="e03d6-113"><dt>**WIA\_SELECT\_DEVICE\_NODEFAULT**</dt></span></span> </dl>               | <span data-ttu-id="e03d6-114">Выполните принудительный вызов метода [**ивиадевмгр:: жетимажедлг**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) или [**IWiaDevMgr2:: жетимажедлг**](-wia-iwiadevmgr2-getimagedlg.md) , чтобы отобразить диалоговое окно **Выбор устройства** .</span><span class="sxs-lookup"><span data-stu-id="e03d6-114">Force the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) or [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method to display the **Select Device** dialog box.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e03d6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e03d6-115">Requirements</span></span>



| <span data-ttu-id="e03d6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e03d6-116">Requirement</span></span> | <span data-ttu-id="e03d6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e03d6-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e03d6-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e03d6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e03d6-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e03d6-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e03d6-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e03d6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e03d6-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e03d6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e03d6-122">Header</span><span class="sxs-lookup"><span data-stu-id="e03d6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e03d6-123"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="e03d6-123"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




