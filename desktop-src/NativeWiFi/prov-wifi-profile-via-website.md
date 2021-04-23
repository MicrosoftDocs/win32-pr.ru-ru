---
title: Подготовка к работе профиля Wi-Fi через веб-сайт
description: Разрешить пользователям скачивать профиль с веб-сайта и подготавливать его.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987857"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a><span data-ttu-id="7117b-103">Подготовка к работе профиля Wi-Fi через веб-сайт</span><span class="sxs-lookup"><span data-stu-id="7117b-103">Provision a Wi-Fi profile via a website</span></span>

<span data-ttu-id="7117b-104">Рабочий процесс, описанный в этом разделе, появился в Windows 10, версия 2004.</span><span class="sxs-lookup"><span data-stu-id="7117b-104">The workflow described in this topic was introduced in Windows 10, version 2004.</span></span> <span data-ttu-id="7117b-105">В этом разделе показано, как настроить веб-сайт таким образом, чтобы пользователь мог подготавливать профиль для Пасспоинт сети (или для обычной сети) перед переходом в диапазон соответствующих точек доступа Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="7117b-105">This topic shows how to configure a website so that a user can provision a profile for a Passpoint network (or for a normal network) prior to moving into range of the corresponding Wi-Fi access points.</span></span> <span data-ttu-id="7117b-106">Примером сценария является то, что пользователь, который может запланировать посещение аэропорта или конференции в первый раз, должен заранее подготовиться, загрузив и подготавливая профиль дома.</span><span class="sxs-lookup"><span data-stu-id="7117b-106">An example scenario is that of a user who might be planning to visit an airport or a conference for the first time, and they want to prepare in advance by downloading and provisioning a profile at home.</span></span>

<span data-ttu-id="7117b-107">Как разработчик вы включаете рабочий процесс, предоставляя XML-профиль и настраивая веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="7117b-107">As a developer, you enable the workflow by providing an XML profile, and configuring a website.</span></span> <span data-ttu-id="7117b-108">После этого пользователи могут подготавливать профиль Wi-Fi, загружая его с веб-сайта через веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="7117b-108">Your users can then provision a Wi-Fi profile by downloading it from your website via a web browser.</span></span> <span data-ttu-id="7117b-109">На устройстве пользователя профиль Wi-Fi подготавливается с помощью активации URI и приложения " **Параметры** Windows".</span><span class="sxs-lookup"><span data-stu-id="7117b-109">On the user's device, the Wi-Fi profile is then provisioned by using URI activation and the Windows **Settings** app.</span></span>

<span data-ttu-id="7117b-110">Этот рабочий процесс заменяет механизм в Internet Explorer для подготовки профилей Wi-Fi, которые основываются на API-интерфейсах JavaScript, зависящих от Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7117b-110">This workflow supersedes the mechanism in Internet Explorer for provisioning Wi-Fi profiles, which relies on Microsoft-specific JavaScript APIs.</span></span> <span data-ttu-id="7117b-111">Этот новый рабочий процесс должен работать со всеми крупными браузерами.</span><span class="sxs-lookup"><span data-stu-id="7117b-111">This new workflow is expected to work with all major browsers.</span></span>

## <a name="the-workflow-in-more-detail"></a><span data-ttu-id="7117b-112">Рабочий процесс более подробно</span><span class="sxs-lookup"><span data-stu-id="7117b-112">The workflow in more detail</span></span>

<span data-ttu-id="7117b-113">Этот рабочий процесс можно активировать из гиперссылки, которая включает в качестве аргумента URI скачивания XML-документа подготовки.</span><span class="sxs-lookup"><span data-stu-id="7117b-113">You can activate this workflow from a hyperlink that includes as an argument the download URI of the provisioning XML document.</span></span>

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

<span data-ttu-id="7117b-114">Например, следующая разметка HTML дает ссылку для установки профилей, которые находятся в гипотетическом документе `http://contoso.com/ProvisioningDoc.xml` .</span><span class="sxs-lookup"><span data-stu-id="7117b-114">For example, the following HTML markup gives a link to install the profile(s) that are found in a hypothetical document `http://contoso.com/ProvisioningDoc.xml`.</span></span>

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

<span data-ttu-id="7117b-115">Ваш XML должен соответствовать схеме подготовки (см. раздел [Подготовка учетных записей](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span><span class="sxs-lookup"><span data-stu-id="7117b-115">Your XML must adhere to the provisioning schema (see [Account provisioning](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span></span> <span data-ttu-id="7117b-116">Ваш XML-файл должен также включать один или несколько элементов [вланпрофиле](./wlan-profileschema-wlanprofile-element.md)   .</span><span class="sxs-lookup"><span data-stu-id="7117b-116">Your XML must also include one or more [WLANProfile](./wlan-profileschema-wlanprofile-element.md) elements.</span></span><span data-ttu-id="7117b-117">Каждый профиль будет отображаться в диалоговом окне **Добавить** , описанном далее.</span><span class="sxs-lookup"><span data-stu-id="7117b-117"> Each profile will be displayed in the **Add** dialog described next.</span></span>

<span data-ttu-id="7117b-118">Когда пользователь щелкает ссылку HTML, Рабочий процесс установки вызывается в приложении " **Параметры** ".</span><span class="sxs-lookup"><span data-stu-id="7117b-118">When the user clicks your HTML link, the installation workflow is invoked in the **Settings** app.</span></span> <span data-ttu-id="7117b-119">XML-документ подготовки загружается приложением " **Параметры** ".</span><span class="sxs-lookup"><span data-stu-id="7117b-119">Your provisioning XML document is downloaded by the **Settings** app.</span></span> <span data-ttu-id="7117b-120">После скачивания будут отображены сведения о профилях, подписи и подписавшем (при условии, что документ соответствует схеме).</span><span class="sxs-lookup"><span data-stu-id="7117b-120">Once it's downloaded, information about the profiles, signature, and signer are displayed (provided that the document adheres to the schema).</span></span>

![Приложение параметров](images/install-dialog.png)

<span data-ttu-id="7117b-122">Кнопка **Добавить** в диалоговом окне приложения **Параметры** доступна только в том случае, если файл подготовки подписан и является доверенным.</span><span class="sxs-lookup"><span data-stu-id="7117b-122">The **Add** button in the dialog in the **Settings** app is enabled only if the provisioning file is signed and trusted.</span></span>

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a><span data-ttu-id="7117b-123">На веб-странице Определите, поддерживается ли этот рабочий процесс</span><span class="sxs-lookup"><span data-stu-id="7117b-123">In your web page, determine whether this workflow is supported</span></span>

<span data-ttu-id="7117b-124">В JavaScript нет способа определить точную версию сборки Windows.</span><span class="sxs-lookup"><span data-stu-id="7117b-124">There is no way in JavaScript to determine the exact build version of Windows.</span></span> <span data-ttu-id="7117b-125">Но если пользователь использует веб-браузер Microsoft ребр, можно определить версию пограничной системы, проверив значение `User-agent` заголовка HTTP.</span><span class="sxs-lookup"><span data-stu-id="7117b-125">But if your user is using the Microsoft Edge web browser, then you can determine the version of Edge by inspecting the value of the `User-agent` HTTP header.</span></span> <span data-ttu-id="7117b-126">Если версия больше или равна `18.nnnnn` , Рабочий процесс поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7117b-126">If the version is greater than or equal to `18.nnnnn`, then the workflow is supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7117b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="7117b-127">Related topics</span></span>

* [<span data-ttu-id="7117b-128">Подготовка учетных записей</span><span class="sxs-lookup"><span data-stu-id="7117b-128">Account provisioning</span></span>](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [<span data-ttu-id="7117b-129">Вланпрофиле, элемент</span><span class="sxs-lookup"><span data-stu-id="7117b-129">WLANProfile element</span></span>](./wlan-profileschema-wlanprofile-element.md)