# ETH-Profit-Mining-
Crypto live Mining profit 
views.py

from django.http import JsonResponse from django.views.decorators.csrf import csrf_exempt from decimal import Decimal

Simulated live mining profit logic

In a real-world scenario, you'd fetch this from a mining API or update it in real time from cron job / background task

@csrf_exempt def live_mining_profit(request): investor_name = "Donald Campolo" # Simulate fetching from database or mining API simulated_profit = Decimal('2352.00')  # Static or computed dynamically

return JsonResponse({
    "investor": investor_name,
    "mining_profit": float(simulated_profit),
})

urls.py

from django.urls import path from .views import live_mining_profit

urlpatterns = [ path('api/mining-profit/', live_mining_profit), ]

