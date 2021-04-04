---
title: Свойство Ивмпараллелпортколлектион Count (Впккоминтерфацес. h)
description: Число параллельных портов в этой коллекции.
ms.assetid: f2f4cac4-bb63-4ac2-ba6e-321a8a29c6d4
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмпараллелпортколлектион
- Ивмпараллелпортколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Count
- IVMParallelPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bb1af40f0e4d15b7eae65e18a8d9910deb769c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988747"
---
# <a name="ivmparallelportcollectioncount-property"></a>Свойство Ивмпараллелпортколлектион:: count

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает число параллельных портов в этой коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Значение свойства

Число параллельных портов.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                            | Значение                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>               | Операция выполнена успешно.<br/> |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl> | Параметр имеет **значение NULL**.<br/>    |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмпараллелпортколлектион определен как 27c3e036-198f-430c-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмпараллелпортколлектион**](ivmparallelportcollection.md)
</dt> </dl>

 

