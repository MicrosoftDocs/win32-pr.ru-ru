---
title: Проверка и инициализация
description: Проверка и инициализация
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- Windows Media Format SDK, проверка
- Windows Media Format SDK, инициализация
- Управление цифровыми правами (DRM), проверка
- DRM (Управление цифровыми правами), проверка
- Управление цифровыми правами (DRM), инициализация
- DRM (Управление цифровыми правами), инициализация
- Расширенные API клиента DRM, проверка
- Расширенные API клиента, проверка
- Расширенные API клиента DRM, инициализация
- Расширенные API клиента, инициализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336375"
---
# <a name="verification-and-initialization"></a><span data-ttu-id="608b6-113">Проверка и инициализация</span><span class="sxs-lookup"><span data-stu-id="608b6-113">Verification and Initialization</span></span>

<span data-ttu-id="608b6-114">Чтобы проверить, разрешено ли шифрование и инициализировать объект, который будет расшифровывать содержимое, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="608b6-114">You should perform the following steps to verify that transcryption is allowed and to initialize an object that will decrypt the content:</span></span>

1.  <span data-ttu-id="608b6-115">Если у вас уже есть идентификатор ключа для содержимого, перейдите к шагу 5.</span><span class="sxs-lookup"><span data-stu-id="608b6-115">If you already have the Key ID for the content, skip to step 5.</span></span>
2.  <span data-ttu-id="608b6-116">Вызовите функцию [**вмкреатидитор**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) , чтобы создать объект редактора метаданных и получить экземпляр интерфейса [**ивмметадатаедитор**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) этого объекта.</span><span class="sxs-lookup"><span data-stu-id="608b6-116">Call the [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) function to create a metadata editor object and get an instance of that object's [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) interface.</span></span>
3.  <span data-ttu-id="608b6-117">Вызовите метод **ивмметадатаедитор:: QueryInterface** , чтобы получить экземпляр интерфейса [**ивмдрмедитор**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) .</span><span class="sxs-lookup"><span data-stu-id="608b6-117">Call **IWMMetadataEditor::QueryInterface** to get an instance of the [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) interface.</span></span>
4.  <span data-ttu-id="608b6-118">Вызовите [**ивмдрмедитор:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) , чтобы получить свойство **DRM \_ дрмхеадер \_ KeyID** .</span><span class="sxs-lookup"><span data-stu-id="608b6-118">Call [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) to get the **DRM\_DRMHeader\_KeyID** property.</span></span>
5.  <span data-ttu-id="608b6-119">Инициализируйте расширенные API клиента DRM Windows Media, вызвав функцию [**вмдрмстартуп**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="608b6-119">Initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>
6.  <span data-ttu-id="608b6-120">Вызовите функцию [**вмдрмкреатепротектедпровидер**](wmdrmcreateprotectedprovider.md) , чтобы создать объект безопасного поставщика и получить экземпляр интерфейса [**ивмдрмпровидер**](iwmdrmprovider.md) этого объекта.</span><span class="sxs-lookup"><span data-stu-id="608b6-120">Call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function to create a secure provider object and get an instance of that object's [**IWMDRMProvider**](iwmdrmprovider.md) interface.</span></span>
7.  <span data-ttu-id="608b6-121">Вызовите метод [**ивмдрмпровидер:: CreateObject**](iwmdrmprovider-createobject.md) , чтобы создать объект управления лицензиями и получить экземпляр его интерфейса [**ивмдрмлиценсеманажемент**](iwmdrmlicensemanagement.md) .</span><span class="sxs-lookup"><span data-stu-id="608b6-121">Call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md) to create a license management object and get an instance of its [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span>
8.  <span data-ttu-id="608b6-122">Вызовите [**ивмдрмлиценсеманажемент:: креателиценсинумератион**](iwmdrmlicensemanagement-createlicenseenumeration.md), передав идентификатор ключа и право, которые управляют действиями, выполняемыми с содержимым после его шифрования.</span><span class="sxs-lookup"><span data-stu-id="608b6-122">Call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing in the Key ID and the right that governs the actions to be taken with the content after it is transcrypted.</span></span> <span data-ttu-id="608b6-123">Этот вызов получит экземпляр интерфейса [**ивмдрмлиценсе**](iwmdrmlicense.md) , который можно использовать для перечисления всех соответствующих лицензий.</span><span class="sxs-lookup"><span data-stu-id="608b6-123">This call will retrieve an instance of the [**IWMDRMLicense**](iwmdrmlicense.md) interface that can be used to enumerate through any matching licenses.</span></span>
9.  <span data-ttu-id="608b6-124">Вызовите [**ивмдрмлиценсе:: жетинклусионлист**](iwmdrmlicense-getinclusionlist.md) , чтобы получить список проверенных систем защиты содержимого (CPS) в соответствии с указаниями издателя лицензии.</span><span class="sxs-lookup"><span data-stu-id="608b6-124">Call [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) to retrieve the list of authorized content protection systems (CPS) as specified by the license issuer.</span></span>
10. <span data-ttu-id="608b6-125">Проанализируйте список включения, чтобы убедиться в том, что идентификатор GUID выходного сервера публикаций Contribute разрешен лицензией.</span><span class="sxs-lookup"><span data-stu-id="608b6-125">Parse the inclusion list to confirm that the GUID of the output CPS is allowed by the license.</span></span>
11. <span data-ttu-id="608b6-126">Если нужный GUID экспорта отсутствует в списке включения, вызовите [**ивмдрмлиценсе:: GetNext**](iwmdrmlicense-getnext.md) , чтобы получить следующую подходящую лицензию (если она есть), и повторите шаги 9 и 10.</span><span class="sxs-lookup"><span data-stu-id="608b6-126">If the desired export GUID is not in the inclusion list, call [**IWMDRMLicense::GetNext**](iwmdrmlicense-getnext.md) to get the next applicable license (if any) and repeat steps 9 and 10.</span></span> <span data-ttu-id="608b6-127">Если ни одна из лицензий не содержит требуемый идентификатор GUID в списке включения, экспорт не может быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="608b6-127">If no license has the desired GUID in its inclusion list, the export cannot be performed.</span></span>
12. <span data-ttu-id="608b6-128">Вызовите метод [**ивмдрмлиценсе:: креатесекуредекриптор**](iwmdrmlicense-createsecuredecryptor.md) , чтобы создать объект дешифратора.</span><span class="sxs-lookup"><span data-stu-id="608b6-128">Call [**IWMDRMLicense::CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) to create a decryptor object.</span></span> <span data-ttu-id="608b6-129">Передайте сертификат экспорта приложения.</span><span class="sxs-lookup"><span data-stu-id="608b6-129">Pass in the export application certificate.</span></span> <span data-ttu-id="608b6-130">Этот вызов предоставит указатель на экземпляр интерфейса [**ивмдрмдекрипт**](iwmdrmdecrypt.md) объекта дешифратора и двоичный объект, содержащий начальное значение.</span><span class="sxs-lookup"><span data-stu-id="608b6-130">This call will provide a pointer to an instance of the decryptor object's [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface and a binary object containing the seed.</span></span> <span data-ttu-id="608b6-131">В данный момент в качестве аргумента параметра *dwFlags* поддерживается только константа **\_ \_ \_ RC4 типа защиты DRM** Windows Media.</span><span class="sxs-lookup"><span data-stu-id="608b6-131">Only the Windows Media **DRM\_PROTECTION\_TYPE\_RC4** constant is supported as an argument to the *dwFlags* parameter at this time.</span></span>
13. <span data-ttu-id="608b6-132">Используйте схему шифрования OAEP RSA для расшифровки вектора инициализации.</span><span class="sxs-lookup"><span data-stu-id="608b6-132">Use the RSA OAEP encryption scheme to decrypt the initialization vector.</span></span>
14. <span data-ttu-id="608b6-133">Используйте библиотеку синтаксического анализа ASF, предоставляемую корпорацией Майкрософт при входе в соглашение Export DRM для Windows Media, чтобы указать смещение в байтах для каждой полезной нагрузки.</span><span class="sxs-lookup"><span data-stu-id="608b6-133">Use the ASF parsing library provided by Microsoft when you enter into the Windows Media DRM export agreement, to locate the offset in bytes for each payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="608b6-134">См. также</span><span class="sxs-lookup"><span data-stu-id="608b6-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="608b6-135">**Экспорт сжатого содержимого**</span><span class="sxs-lookup"><span data-stu-id="608b6-135">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




