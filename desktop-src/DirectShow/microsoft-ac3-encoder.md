---
description: Фильтр кодировщика Microsoft AC-3 кодирует аудио стерео PCM в Dolby Digital битовый поток.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Кодировщик Microsoft AC-3 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35984975fc5a56b043f1b2ceda56505ee6fe74038034fb35deb09b6a5f6a0f41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153172"
---
# <a name="microsoft-ac-3-encoder"></a>Кодировщик Microsoft AC-3

Фильтр кодировщика Microsoft AC-3 кодирует аудио стерео PCM в Dolby Digital битовый поток.

> [!Note]  
> Реализация технологий Dolby Digital в корпорации Майкрософт ограничена условиями программы цифрового лицензирования Dolby, используемой приложениями Майкрософт.

 

> [!Note]  
> Этот фильтр не поддерживается на платформах на базе IA-64.

 



Сведения о фильтре

Интерфейсы фильтра

[**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

Типы носителей входных закрепления

**MEDIATYPE \_ Аудио**, **медиасубтипе \_ PCM**<br/> Тип входных данных должен составлять 48-кГц стерео, 16 бит на выборку.<br/>

Интерфейсы входных закрепления

[**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Типы носителей для выходного ПИН-кода

**MEDIATYPE \_ Аудио**, **медиасубтипе \_ Dolby \_ AC3**<br/> **MEDIATYPE \_ Stream**, **медиасубтипе \_ Dolby \_ AC3**<br/>

Интерфейсы выходного ПИН-кода

[**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Фильтровать CLSID

**Идентификатор CLSID \_ CMSAC3Enc** (объявлено в вмкодекдсп. h)

Исполняемый объект

msac3enc.dll

[Заслуживают](merit.md)

**\_ \_ не \_ использовать**

[Категория фильтра](filter-categories.md)

**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**



 

## <a name="remarks"></a>Remarks

Этот фильтр недоступен для использования сторонними приложениями.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows главная Premium vista, Windows vista Ultimate, Windows 7 Домашняя расширенная, Windows 7 Профессиональная, Windows 7 Корпоративная, Windows 7 Максимальная \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>См. также

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




