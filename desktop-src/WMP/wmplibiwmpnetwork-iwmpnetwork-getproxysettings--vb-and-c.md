---
title: Ивмпнетворк Жетпроксисеттингс, метод
description: Метод Жетпроксисеттингс возвращает сведения о параметрах прокси-сервера для протокола.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- Жетпроксисеттингс метод Windows Media Player
- Жетпроксисеттингс метод проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, метод Жетпроксисеттингс
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668850"
---
# <a name="iwmpnetworkgetproxysettings-method"></a><span data-ttu-id="f0be0-106">Метод Ивмпнетворк:: Жетпроксисеттингс</span><span class="sxs-lookup"><span data-stu-id="f0be0-106">IWMPNetwork::getProxySettings method</span></span>

<span data-ttu-id="f0be0-107">Метод **жетпроксисеттингс** возвращает сведения о параметрах прокси-сервера для протокола.</span><span class="sxs-lookup"><span data-stu-id="f0be0-107">The **getProxySettings** method returns information about the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0be0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0be0-108">Syntax</span></span>


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a><span data-ttu-id="f0be0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0be0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0be0-110">*бстрпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f0be0-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0be0-111">**Строка System. String** , которая является именем протокола.</span><span class="sxs-lookup"><span data-stu-id="f0be0-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="f0be0-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f0be0-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0be0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0be0-113">Return value</span></span>

<span data-ttu-id="f0be0-114">Значение **System. Int32** , которое является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f0be0-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="f0be0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f0be0-115">Value</span></span> | <span data-ttu-id="f0be0-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f0be0-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f0be0-117">0</span><span class="sxs-lookup"><span data-stu-id="f0be0-117">0</span></span>     | <span data-ttu-id="f0be0-118">Прокси-сервер не используется.</span><span class="sxs-lookup"><span data-stu-id="f0be0-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="f0be0-119">1</span><span class="sxs-lookup"><span data-stu-id="f0be0-119">1</span></span>     | <span data-ttu-id="f0be0-120">Используются параметры прокси-сервера для текущего браузера (допустимы только для HTTP).</span><span class="sxs-lookup"><span data-stu-id="f0be0-120">The proxy settings for the current browser are being used (valid only for HTTP).</span></span> |
| <span data-ttu-id="f0be0-121">2</span><span class="sxs-lookup"><span data-stu-id="f0be0-121">2</span></span>     | <span data-ttu-id="f0be0-122">Используются заданные вручную параметры прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="f0be0-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="f0be0-123">3</span><span class="sxs-lookup"><span data-stu-id="f0be0-123">3</span></span>     | <span data-ttu-id="f0be0-124">Параметры прокси-сервера обнаруживаются в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="f0be0-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="f0be0-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0be0-125">Remarks</span></span>

<span data-ttu-id="f0be0-126">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="f0be0-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="f0be0-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="f0be0-127">Examples</span></span>

<span data-ttu-id="f0be0-128">В следующем примере кода используется **жетпроксисеттингс** для вывода сообщения, которое предоставляет сведения о текущих параметрах прокси-сервера проигрывателя в метке.</span><span class="sxs-lookup"><span data-stu-id="f0be0-128">The following code example uses **getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in a label.</span></span> <span data-ttu-id="f0be0-129">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="f0be0-129">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a><span data-ttu-id="f0be0-130">Требования</span><span class="sxs-lookup"><span data-stu-id="f0be0-130">Requirements</span></span>



| <span data-ttu-id="f0be0-131">Требование</span><span class="sxs-lookup"><span data-stu-id="f0be0-131">Requirement</span></span> | <span data-ttu-id="f0be0-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f0be0-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0be0-133">Версия</span><span class="sxs-lookup"><span data-stu-id="f0be0-133">Version</span></span><br/>   | <span data-ttu-id="f0be0-134">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f0be0-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f0be0-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f0be0-135">Namespace</span></span><br/> | <span data-ttu-id="f0be0-136">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="f0be0-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f0be0-137">Сборка</span><span class="sxs-lookup"><span data-stu-id="f0be0-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f0be0-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f0be0-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0be0-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0be0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0be0-140">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f0be0-140">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f0be0-141">**Ивмпнетворк. setProxySettings (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f0be0-141">**IWMPNetwork.setProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





