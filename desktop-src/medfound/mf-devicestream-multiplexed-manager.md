---
description: Предоставляет экземпляр Имфмуксстреаматтрибутесманажер, который управляет Имфаттрибутес, описывающим подпотоки мультиплексированного источника мультимедиа.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: Атрибут MF_DEVICESTREAM_MULTIPLEXED_MANAGER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647240"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a>\_Атрибут девицестреам \_ мультиплексированного \_ диспетчера MF

Предоставляет экземпляр [**имфмуксстреаматтрибутесманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) , который управляет [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , описывающим подпотоки мультиплексированного источника мультимедиа.

## <a name="data-type"></a>Тип данных

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Комментарии

Передайте это значение в [**имфаттрибутес:: Ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) , чтобы определить, предоставляет ли источник мультимедиа мультиплексированные потоки, и, если это так, получите экземпляр [**имфмуксстреаматтрибутесманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                          |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



 

 
