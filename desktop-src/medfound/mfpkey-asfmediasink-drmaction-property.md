---
description: указывает, как приемник мультимедиа ASF должен применяться Windows media DRM.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: Свойство MFPKEY_ASFMEDIASINK_DRMACTION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed62f62a5d03d7fe938101d9837bd8ed9bccefe69b2bf30e0566ea0b471e37f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874348"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>МФПКЭЙ \_ асфмедиасинк \_ дрмактион, свойство

указывает, как приемник мультимедиа ASF должен применяться Windows media DRM.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**ULONG**

VT \_ UI4

**улвал**



## <a name="remarks"></a>Remarks

Значение этого свойства является членом перечисления [**мфсинк \_ вмдрмактион**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) .

Этот атрибут можно использовать для настройки приемника мультимедиа ASF. Использование зависит от того, какая функция вызывается для создания приемника мультимедиа ASF:

-   [**Мфкреатеасфмедиасинк**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): запросите полученный указатель [**Имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) для интерфейса **ипропертисторе** .

-   [**Мфкреатеасфмедиасинкактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): вызов [**Имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) в указателе [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , указанном в параметре *pContentInfo* .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
