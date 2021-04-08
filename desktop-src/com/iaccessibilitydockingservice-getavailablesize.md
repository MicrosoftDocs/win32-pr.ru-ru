---
title: Иакцессибилитидоккингсервице Жетаваилаблесизе, метод
description: Возвращает размеры, доступные для закрепления окна специальных возможностей на мониторе.
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- COM-метод Жетаваилаблесизе
- Метод Жетаваилаблесизе COM, интерфейс Иакцессибилитидоккингсервице
- Интерфейс Иакцессибилитидоккингсервице COM, метод Жетаваилаблесизе
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068942"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a>Метод Иакцессибилитидоккингсервице:: Жетаваилаблесизе

Возвращает размеры, доступные для закрепления окна специальных возможностей на мониторе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хмонитор* \[ окне\]
</dt> <dd>

Указывает монитор, для которого будет получен доступный размер закрепления.

</dd> <dt>

*пумаксхеигхт* \[ заполняет\]
</dt> <dd>

При успешном выполнении задайте максимальную высоту, доступную для закрепления на заданном *хмонитор*, в пикселях.

В случае сбоя установите нулевое значение.

</dd> <dt>

*пуфикседвидс* \[ заполняет\]
</dt> <dd>

При успешном выполнении задайте фиксированную ширину, доступную для закрепления в заданном *хмонитор*, в пикселях. Любое окно, прикрепленное к этому *хмонитор* , будет иметь ширину.

В случае сбоя установите нулевое значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение



| Код возврата                                                                                                                          | Описание                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                                                 | Успешно.<br/>                                                              |
| <dl> <dt>**HRESULT \_ из \_ Win32 (ошибка: \_ Недопустимый \_ \_ маркер монитора)**</dt> </dl> | Монитор, указанный в обработчике монитора, не поддерживает прикрепление.<br/> |



 

Если либо *пумаксхеигхт* , либо *пуфикседвидс* имеют значение null, произойдет нарушение прав доступа.

## <a name="remarks"></a>Комментарии

Окна специальных возможностей могут быть прикреплены только к монитору, который содержит не менее 768 вертикальных пикселей на экране. Этот API не позволяет закреплять такие окна с высотой, что приведет к тому, что приложения Магазина Windows будут иметь менее 768 вертикальных пикселей на экране.

## <a name="examples"></a>Примеры


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иакцессибилитидоккингсервице**](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





