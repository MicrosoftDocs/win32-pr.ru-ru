---
description: Указывает имя семейства пакетов приложений для приложения конфигурации виртуальной камеры.
title: Атрибут MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME (Мфапи. h)
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691869"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a><span data-ttu-id="cc59c-103">\_ \_ \_ \_ Атрибут имени семейства пакетов приложений MF виртуалкамера \_</span><span class="sxs-lookup"><span data-stu-id="cc59c-103">MF\_VIRTUALCAMERA\_APP\_PACKAGE\_FAMILY\_NAME attribute</span></span>

<span data-ttu-id="cc59c-104">Указывает имя семейства пакетов приложений для приложения конфигурации виртуальной камеры.</span><span class="sxs-lookup"><span data-stu-id="cc59c-104">Specifies the app package family name for a virtual camera configuration application.</span></span> <span data-ttu-id="cc59c-105">если этот параметр указан, конвейер свяжет приложение конфигурации с виртуальной камерой и предоставит точку запуска на странице Параметры камеры.</span><span class="sxs-lookup"><span data-stu-id="cc59c-105">When provided, the pipeline will associate the configuration application with the virtual camera and provide a launch point within the Camera Settings page.</span></span>

## <a name="data-type"></a><span data-ttu-id="cc59c-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc59c-106">Data type</span></span>

[<span data-ttu-id="cc59c-107">MF_ATTRIBUTE_STRING</span><span class="sxs-lookup"><span data-stu-id="cc59c-107">MF_ATTRIBUTE_STRING</span></span>](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a><span data-ttu-id="cc59c-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc59c-108">Remarks</span></span>

<span data-ttu-id="cc59c-109">Этот атрибут может быть предоставлен с помощью настраиваемого источника мультимедиа виртуальной камеры из источника данных в хранилище атрибутов [имфмедиасаурцеекс:: жетсаурцеаттрибутес](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span><span class="sxs-lookup"><span data-stu-id="cc59c-109">This attribute may be exposed by the virtual camera custom media source from the media source attribute store [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span></span>  

<span data-ttu-id="cc59c-110">Если приложение конфигурации еще не установлено на компьютере, приложение магазина будет запущено и откроется страница приложения, указанная с помощью имени семейства пакетов.</span><span class="sxs-lookup"><span data-stu-id="cc59c-110">If the configuration application is not yet installed on the machine, the Store application will be launched and navigated to the application page specified by the package family name.</span></span> <span data-ttu-id="cc59c-111">В противном случае установленное приложение будет запущено для пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc59c-111">Otherwise, the installed application will be launched for the user.</span></span>


## <a name="requirements"></a><span data-ttu-id="cc59c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="cc59c-112">Requirements</span></span>



| <span data-ttu-id="cc59c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="cc59c-113">Requirement</span></span> | <span data-ttu-id="cc59c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="cc59c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cc59c-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc59c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cc59c-116">Windows Сборка 22000</span><span class="sxs-lookup"><span data-stu-id="cc59c-116">Windows Build 22000</span></span><br/>                          |
| <span data-ttu-id="cc59c-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc59c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cc59c-118">Windows Сборка 22000</span><span class="sxs-lookup"><span data-stu-id="cc59c-118">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="cc59c-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cc59c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc59c-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc59c-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc59c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc59c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc59c-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc59c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cc59c-123">**Имфаттрибутес:: GetString**</span><span class="sxs-lookup"><span data-stu-id="cc59c-123">**IMFAttributes::GetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="cc59c-124">**Имфаттрибутес:: SetString**</span><span class="sxs-lookup"><span data-stu-id="cc59c-124">**IMFAttributes::SetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




