---
description: Освобождает блок памяти, выделенный из кучи с помощью Ртлаллокатехеап.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: Функция Ртлфрихеап (Нтифс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e51994c4bcd941bc96575eb3fdbb45d4111c1aeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538843"
---
# <a name="rtlfreeheap-function"></a>Функция Ртлфрихеап

Освобождает блок памяти, выделенный из кучи с помощью [**ртлаллокатехеап**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).

## <a name="syntax"></a>Синтаксис


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Хеафандле* \[ окне\]
</dt> <dd>

Маркер для кучи, блок памяти которого должен быть освобожден. Этот параметр является маркером, возвращаемым функцией [**ртлкреатехеап**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).

</dd> <dt>

*Флаги* \[ в необязательное\]
</dt> <dd>

Набор флагов, управляющих аспектами освобождения блока памяти. Указание следующего значения переопределяет соответствующее значение, указанное в параметре *flags* , когда куча была создана с помощью [**ртлкреатехеап**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).



| Flag                           | Значение                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| КУЧА \_ без \_ сериализации<br/> | Взаимное исключение не будет использоваться, если **ртлфрихеап** обращается к куче. <br/> |



 

</dd> <dt>

*Хеапбасе* \[ окне\]
</dt> <dd>

Указатель на блок памяти для освобождения. Этот указатель возвращается функцией [**ртлаллокатехеап**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если блок был успешно освобожден; В противном случае — **значение false** .

> [!Note]  
> Начиная с Windows 8 возвращаемое значение типизировано как **логическое**, имеющее размер, отличный от **логического**.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                                                    |
| Целевая платформа<br/>          | <dl> <dt>[Универсальной](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>Нтифс. h (включение Нтифс. h)</dt> </dl>                                    |
| Библиотека<br/>                  | <dl> <dt>NTDLL. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ртлаллокатехеап**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[**ртлкреатехеап**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[**ртлдестройхеап**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
